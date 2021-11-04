Title: C++ 14 : The new stuff
Date: 2015-10-02 13:16
Category: programming
Tags: cpp, cpp11, til
Authors: Bhargav Bhat
Summary: TIL about the C++14 release and the new features in this release

Sometime last year the C++14 standard was finalized. Although, this is specified to be a minor release to the standard, it does bring some very helpful features. As I understand, new versions of most compilers support these features in some form already and it is just a matter of using the right switch to have them behave as per the C++14 standard (rather than whatever implementation specific behaviour they implemented as an extension).

### "New" New Stuff

There aren't too many "new" new features, the ones I found most helpful are:

- **Binary Literals** : `0b` or `0B` can now be used to specify binary literals (similar to how hex numbers are specified). This is pretty helpful for specifying masks and such
- **Digit Separator** : `'` (single quote) can now be used between numbers to separate digits, eg: 100k can be written `100'000`
- **STL Custom Literals** : STL has been extended to support string literals such as `s` for seconds etc for various types

### Old New Stuff

With a nod to the [inspiration](https://devblogs.microsoft.com/oldnewthing/) behind this title, here's the list of C++11 items that 14 improves upon:

- **Return-type Deduction** : `auto` is now permissible as a return type. Eg: `auto someFunc(int x, float y);`
- **Generic Lambdas** : `auto` is now permissible in lambda parameter type. Eg: `[](auto x, auto y) {return x + y;};`
- **Generic Lambda Caputure** : In addition to capturing scoped variables by value, now, arbitrary values can also be passed into lambdas. Eg: `[a = x, b = x+1] {return 2*a+b;}`

[This](https://www.infoq.com/news/2014/08/cpp14-here-features/) and [this](https://isocpp.org/wiki/faq/cpp14-language) page have been very helpful to bring me upto speed with C++14.

Overall, C++14 seems to be an "hotfix" or "service pack" for C++11 rather than something major. It should be realtively simple to migrate existing C++11 code to 14 and start utilizing some of the new stuff from 14. While binary literals and generic lambdas look great on paper, I really am keen to see how much of an impact they really have on day-to-day tasks.
