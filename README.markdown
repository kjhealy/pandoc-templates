# Pandoc Configuration and Support Files

## Description

A collection of support files for use with Pandoc, and specifically for helping to turn pandoc markdown files into nice HTML, LaTeX, and PDF output. These files go in your `~/.pandoc/` folder and are designed to work with the style and configuration material provided in [latex-custom-kjh](https://github.com/kjhealy/latex-custom-kjh/), [socbibs](https://github.com/kjhealy/socbibs), and the [Emacs Starter Kit for the Social Sciences](https://kieranhealy.org/resources/emacs-starter-kit). The only real dependencies are the latex class and style files in [latex-custom-kjh](http://github.com/kjhealy/latex-custom-kjh), however.


PDF                        |HTML                       | Word
:-------------------------:|:-------------------------:|:-------------------------:
![](examples/screenshots/pdf_output.png)  |  ![](examples/screenshots/html_output.png )  |  ![](examples/screenshots/docx_output.png)

![Sample PDF template](examples/screenshots/pdf_output.png  "Sample PDF template")

## Notes

What's included?

- Some [Pandoc](http://johnmacfarlane.net/pandoc/) templates for an
  article in PDF (vita LaTeX), HTML, or Microsoft Word. These go in
  `~/.pandoc/templates`. These can be be pointed to directly with the
  `--template=` switch as appropriate. The `latex.template` and
  `xelatex.template` depend on the style files in
  [latex-custom-kjh](https://github.com/kjhealy/latex-custom-kjh/).
  The Word reference documents depend on you having Myriad Pro and
  Minion Pro installed.
- In R, knitr's `knit()` function will turn `.Rmd` files into `.md`
  files. The configuration file in the `knitr/` folder is an example
  to help you produce HTML or `.tex` using knitr's `pandoc()` helper
  function.
- The CSL files in the `csl/` folder format the bibliography generated
  by pandoc and citeproc. (For simplicity we avoid dealing with
  biblatex directly at all.) The `chicago-syllabus.csl` file makes a
  tiny change to a standard Chicago Notes CSL file so you can use it
  to output citation information in the body text of a document. This
  makes it useful for lists of references in CVs and course
  syllabuses. The other two files are APSA and AJPS standard files
  from the main
  [CSL styles repository](https://github.com/citation-style-language/styles).
- The Makefile in the `makefile/` folder helps you generate HTML,
  LaTeX, and PDF output from your markdown files in a convenient
  way. It is meant to go in the folder where you are writing your
  paper. It looks for `.md` files in the working directory and
  converts them to nice HTML, PDF, and LaTeX files using the templates
  provided here, the style files in
  [latex-custom-kjh](https://github.com/kjhealy/latex-custom-kjh/), and
  the bibliography files in
  [socbibs](https://github.com/kjhealy/socbibs). You can of course
  change the bibliography and template files as desired.
- The `pandoc` commands produced by the current version of the `Makefile` include switches that invoke two [pandoc filters](http://pandoc.org/scripting.html) that do additional processing on the bibliography and cross-references in the document. You should install [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref) and [pandoc-citeproc-preamble](https://github.com/spwhitton/pandoc-citeproc-preamble) to make these work.
- The [md-article-starter](https://github.com/kjhealy/md-starter) repository is a basic project folder you can clone that gives you a template for an article written in Markdown and a `Makefile` to produce `.html`, `.tex` or `.pdf` output from it. For R users there is an [rmd-article-starter](https://github.com/kjhealy/rmd-starter) as well, which begins with an `.Rmd` file.

## Contact
Kieran Healy, `@kjhealy`
