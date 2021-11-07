Title: Working Effectively with Legacy Code : A Review
Date: 2019-12-30 21:44
Category: programming
Tags: book-review
Authors: Bhargav Bhat
Summary: My review of Working Effectively with Legacy Code

This is my summary of takeaways from the book Working Effectively with Legacy Code, written by Micheal Feathers. I purchased a 2004 re-print in paperback with ISBN 978-0131177055. Paper quality was good and I did not have any issues with highlighter ghosting, but the binding seems a bit suspect. Probably will have to liberally employ paper glue and tape to mend it. The content of the book itself was pretty good. The key takeaways were:


- Add tests first, changing as little of the code as possible to facilitate testing
- Identify **seams** and start adding tests from these seams
- Tests should be quick to run and should not involve communication with external components (network, DB etc)
- **Characterization Tests** : tests as a means of ensuring correctness and documenting the code (behaviour and understanding of the codebase)
- _extract interfaces_ and _parameterized constructors_ as tools for breaking dependencies

Overall, the book was a decent read discussing specific techniques that could be put into use right away. The overarching theme was refactoring while minimizing risk, i.e safely isolating changes and confidently refactoring an existing codebase without much in the way of useful documentation on tests.
