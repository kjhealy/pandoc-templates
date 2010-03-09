# Pandoc Templates 

## Description

Some very rudimentary [pandoc](http://johnmacfarlane.net/pandoc/) templates, meant to go in `~/.pandoc/templates`, be pointed to directly with the `--template=` or `--css` switches as appropriate, and used with what's provided in [latex-custom-kjh](http://kjhealy.github.com/latex-custom-kjh/). 

Pandoc is really terrific and, I find, much more flexible than MultiMarkdown. So I've started to experiment with it a bit. Taking advantage of its capabilities in Emacs is made easier by Joost Kremers' [pandoc minor-mode](http://user.uni-frankfurt.de/~kremers/pandoc-mode.html). The latter is included with my fork of the [Emacs Starter Kit](http://kjhealy.github.com/emacs-starter-kit/).

## Notes

-   The CSS template is a first cut at getting an article-like
    format similar to the layout of my own website.
-   The xetex template is meant to be used with everything provided
    in [latex-custom-kjh](http://github.com/kjhealy/latex-custom-kjh).
    If you rename `article-xelatex.template` or `referee-xelatex.template` 
	to `latex.template` in `~/.pandoc/templates/` it will override 
	pandoc's default template (and very likely break any setup that doesn't 
	look just like mine).


## Contact
Kieran Healy, kjhealy@gmail.com
