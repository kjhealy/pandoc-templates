# Pandoc Templates, CSS files, and 

## Description

Some very rudimentary [Pandoc](http://johnmacfarlane.net/pandoc/) templates, meant to go in `~/.pandoc/templates`, be pointed to directly with the `--template=` or `--css` switches as appropriate, and used with what's provided in [latex-custom-kjh](http://kjhealy.github.com/latex-custom-kjh/). I also set pandoc up to work with the  [Marked](http://markedapp.com/) app, a handy HTML live previewer for `.md` files.

I use these files together with my [Social Science Starter Kit](http://kjhealy.github.com/emacs-starter-kit/) for Emacs.

## Notes

- The xetex template is meant to be used with everything provided in
    [latex-custom-kjh](http://github.com/kjhealy/latex-custom-kjh).
    If you rename `article-xelatex.template` or
    `referee-xelatex.template` to `latex.template` in
    `~/.pandoc/templates/` it will override pandoc's default template
    (and very likely break any setup that doesn't look just like
    mine).
- The `css` files in the `marked/` folder are meant to be used
    together with pandoc and [Marked](http://markedapp.com/). The shell script in there,
    `panmarked.sh` is what I tell Marked to use to create its
    HTML. You point to it in Marked > Preferences > Behavior. The CSS
    files can be added in Marked > Style > Custom CSS.
- The configuration file in the `knitr/` folder is an example to help
  you produce HTML or `.tex` from inside R, using knitr and its `pandoc()` helper function.


## Contact
Kieran Healy, kjhealy@gmail.com
