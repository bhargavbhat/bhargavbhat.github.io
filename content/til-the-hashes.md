Title: The Hashes
Date: 2011-10-08 13:22
Category: programming
Tags: c, preprocessor, til
Authors: Bhargav Bhat
Summary: TIL about the # (Stringizing) and ## (Concatenation) operators of the Pre-processor

I ran into a seemingly straight forward problem earlier this week: treat a particular `#define` value as either string or int, depending on the context where it is used. A naive solution to is repeating the `#define` twice, once as a string and then as a integer:

	#!c
	#define SOME_VALUE_INT 42
	#define SOME_VALUE_STR "42"

... and using the right value depending on the context. Not only is this naive method a violation of DRY, but it is also very crude and inelegant. Having multiple such `#define`ed constants are a maintainance disaster waiting to happen. My search for a better way to deal with this lead me to a very relevant [question](https://stackoverflow.com/questions/2653214/stringification-of-a-macro-value) on SO and down I went the rabbit hole that is the the C Pre-processor. This is a summary of my learning and notes for my future self.

###The Stringizing Operator : `#`

This operator solves the problem above rather elegantly, as described the accepted answer to in the SO question above:
	
	#!c
	#define xstr(a) str(a)
	#define str(a) #a

	#define RECORDS_PER_PAGE 10

	#define REQUEST_RECORDS \
    		"SELECT Fields FROM Table WHERE Conditions" \
        	" OFFSET %d * " xstr(RECORDS_PER_PAGE) \
	    	" LIMIT " xstr(RECORDS_PER_PAGE) ";"

The `#` operator:

- allows the preprocessor to replace anything prefixed with a `#` with the literal text of the actual argument. The argument is not macro-expanded.
- leading & trailing whitespace is ignored. Whitespaces in the middle of the text converted to a single space
- to stringize the result of expansion of a macro argument, you have to use two levels of macros

*Source* : GCC [docs](https://gcc.gnu.org/onlinedocs/cpp/Stringizing.html#Stringizing)

###The Concatenation Operator : `##`

This operator solves a somewhate related problem of merging or combining two macro values into a single string. The `##` operator:

- performs token pasting : two tokens on either side of ‘##’ operator are combined into a single token. The the actual arguments are not macro-expanded.
- cannot create a comment by concatenating ‘/’ and ‘*’.
- comments in arguments that will be concatenated

*Source* : GCC [docs](https://gcc.gnu.org/onlinedocs/cpp/Concatenation.html#Concatenation)

While these operators present interesting possibilities, using them for all but the most basic and straight forward needs would be difficult. Although handy in a few situations, they are qutie limited and come with a bunch of caveats. However, there still are a few corner cases where they do make lives of programmers a lot simpler.
