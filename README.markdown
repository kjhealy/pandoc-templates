# Pandoc Templates and CSS files, Knitr Config Example

## Description

Some rudimentary [Pandoc](http://johnmacfarlane.net/pandoc/) templates, meant to go in `~/.pandoc/templates`, be pointed to directly with the `--template=` or `--css` switches as appropriate, and used with what's provided in [latex-custom-kjh](http://kjhealy.github.com/latex-custom-kjh/). I also set pandoc up to work with the  [Marked](http://marked2app.com/) app, a very handy HTML live previewer for markdown files. This used to be done with a shell script (in the original Marked app) but that's no longer necessary.

I use these files together with my [Social Science Starter Kit](http://kjhealy.github.com/emacs-starter-kit/) for Emacs.

## Notes

- The `latex.template` and `xelatex.template` files are meant to be
    used with everything provided in
    [latex-custom-kjh](http://github.com/kjhealy/latex-custom-kjh).
- The `css` files in the `marked/` folder are meant to be used
    together with pandoc and [Marked](http://markedapp.com/). The
    shell script in the `marked/` folder, `panmarked.sh` is what I
    previously had Marked use as a custom processor to create its
    HTML. You point to it in Marked > Preferences > Behavior. In the
    current version of the application, Marked 2, I still enable a
    custom processor in Marked > Preferences > Behavior. But now
    instead of using a shell script I simply specify the Path to
    Pandoc like this (e.g.): `/usr/bin/pandoc` and the various
    switches and arguments to pandoc in the 'Args' field below it,
    like this:
    
    ```
    -r markdown+simple_tables+table_captions+yaml_metadata_block -w html
    -s -S --template=/Users/kjhealy/.pandoc/templates/html.template
    --filter pandoc-citeproc
    --bibliography=/Users/kjhealy/Documents/bibs/socbib-pandoc.bib
    ```
    
    Then I tell Marked to use this by default.
- The CSS files can be added in Marked > Style > Custom CSS. Marked
  can then use them to format the HTML output.
- The configuration file in the `knitr/` folder is an example to help
  you produce HTML or `.tex` from inside R, using knitr and its `pandoc()` helper function.
- The CSL file in the `csl/` folder makes a tiny change to a Chicago Notes CSL file so you 
  can use it to output citation information in the body text of a document. This makes
  it useful for lists of references in CVs and course syllabuses. 


## Contact
Kieran Healy, `kjhealy@gmail.com`
