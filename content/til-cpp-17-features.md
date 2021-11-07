Title: C++ 17 Features
Date: 2018-01-26 19:57
Category: programming
Tags: cpp, cpp11, til
Authors: Bhargav Bhat
Summary: TIL about the C++17 release and some of the new features in the language and the STL

Sometime last year the C++17 standard was finalized, although there weren't too many new features in the language itself that were relevant to an application developer focused on embedded and resource constrained development, there were three that stood out:

- **Guaranteed Copy-Elision** : Essentially, the standard now mandates RVO, although most compilers were already doing this anyway
- **`constexpr` can be used with `if`** : An interesting feature that can eliminate a bunch of `#ifdef`s, this allows programmers to use `constexpr` with regular `if` to compile only relevant bits of code at compile time
- **Initializers in `if` and `switch`** : Similar to an `using` block in other languages, this facility permits programmers to initailize & use variables within the `if`/`else` blocks. Variables are automatically destroyed at the end of said block

Apart from this, the STL received a few important new additions, which I would need to go over closely :

- `std::variant`
- `std::any`
- `std::optional`
- `std::string_view`

An indepth summary of these features can be found [here](https://www.modernescpp.com/index.php/cpp17-core) and [here](https://blogs.grammatech.com/new-features-of-c17).

Overall, C++17 has added more stuff than C++14, however, a lot of it is for niche or narrow usecases. I would need to understand the changes more in the upcoming days to see how best these can be leveraged in the current context.
