Title: Overleaf - Online LaTeX Editor
Date: 2014-11-01 20:33
Category: tools
Tags: latex, til
Authors: Bhargav Bhat
Summary: TIL about Overleaf the online LaTeX Editor

I've been using [LaTeX](https://www.latex-project.org/about/) to typeset my resume for a while. The advantages are many:

- Plain-text format, can be added into version control
- Relatively easy to export to multiple formats : PDF, Word (via `pandoc`)
- Precise positioning of elements and easier to possible to tweak formatting of certain sections or parts without ruining the formatting of the entire document
- Reuse and Automation (environments and commands etc)

My resume is based on a modified version of this [template](https://github.com/treyhunner/resume) and is a simple 2-pager without too many custom elements. However, to compile and generate it on the fly meant I would need an installation of LaTeX on my laptop or a VM that I could SSH into. This was a minor incovenience, that could be worked around by having a compiled PDF in the same repo as the resume itself and that's precisely what I did until I learnt about [Overleaf](https://www.overleaf.com).

Overleaf is an awesome website that lets you import existing LaTeX projects and provides the facility to compile them into a PDF that you can download. It also has rudimentary form of workspace separation and limted version control/history features. Where I found it lacking was on the collaboration front, as far as I can see there is no straightforward way to "invite" people to edit or review your files (a-la Google Docs) and nor is there a way to send or share the final output PDF with users via email (short of downloading the PDF yourself and sharing that directly). I sure do hope they add these features soon :) 

PS: Obligatory LaTeX resume [joke](http://stevehanov.ca/blog/?id=56).
