Title: More Effective C++ & Effective STL : Book Reviews
Date: 2012-12-22 10:13
Category: programming
Tags: cpp, book-review
Authors: Bhargav Bhat
Summary: My review of the More Effective C++ & Effective STL Books

With more of my day-to-day work moving to C++, I was looking for a nice book to help me get upto speed with C++, best practices and some of the gotchas that C++ is ~famous~ infamous for. This book in particular had rave reviews and was recommended by multiple people, with colleagues, former colleagues and internet strangers all saying very good things about it. I purchased by copy from Sapna Book House about 2 months ago and have been reading it on and off since. I just finished the last topic ("Item 55") a few hours ago.

### More Effective C++

The copy I purchased (online, this time around, those deals are too good to ignore) is a 2002 reprint (ISBN: 978-81-7758-980-1) as a paperback. The paper was mediocre as the pages were pretty flimsy. Unlike the first instalment of the book, this one had major issues with ghosting of highlighted parts.

As with the first part of the series, this book too is divided into multiple sections and each section has a bunch of topics, and again there were no exercises as such. Of the 35 Items presented, the following were the most appealing/relevant to my circumstances

- Item 2  : Prefer C++ style casts 
- Item 3  : Never treat arrays polymorphically
- Item 5  : Be wary of user conversion functions
- Item 9  : Use destructors to prevent resource leaks
- Item 13 : Catch exceptions by reference
- Item 15 : Understand costs of exception handling
- Item 18 : Amortize the cost of expected computation
- Item 20 : Facilitate return-value optimization (RVO)
- Item 28 : Smart Pointers
- Item 33 : Make non-leaf classes abstract

### Effective STL

Was much of the same stuff as the previous two books in this series. This was once again a 2002 reprint (ISBN: 978-81-7758-908-5) paperback. Paper quality was better than More Effective C++ but I did encounter slight ghosting of highlights. While most of the content in Effective STL was virtually new to me, I found these items the most helpful, out of the total 50 presented:

- Item 3  : Make copying cheap & correct for containers
- Item 6  : Be alert for C++'s most vexing parse 
- Item 8  : Never create containers of `auto_ptr`s
- Item 9  : Choose carefully among erasing options
- Item 13 : Prefer `vector` and `string` to dynamically allocated arrays
- Item 14 : Use `reserve` to avoid unnecessary reallocations
- Item 18 : Avoid using `vector<bool>`
- Item 19 : Understand differences between `equality` and `equivalence`
- Item 24 : Choose carefully between `map::operator[]` and `map::insert` when efficiency is important
- Item 27 : Use `distance` and `advance` to convert `const_iterator`s to `iterator`s
- Item 32 : Follow `remove`-like algorithms by `erase` if you really want to remove something
- Item 36 : Understand the proper implementation of `copy_if`
- Item 41 : Understand the reasons for `ptr_fun`, `mem_fun` and `mem_fun_ref`
- Item 49 : Learn to decipher STL-related compiler diagonostics


Overall, I'd consider that both books lived up to the hype surrounding them and the first installment in the series. Unlike the first part, these were focused a lot more on techniques and features beyond the basics. Between the two, More Effective C++ was a bit of heavy/intensive read esp. towards the end.  
