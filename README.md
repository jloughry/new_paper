Joe Loughry (joe.loughry@stx.ox.ac.uk)
===========

This is a template for a new journal or conference paper; the idea is to
copy this&mdash;ideally, automatically&mdash;and base the new paper off it.

How to Create a New Git Repository
----------------------------------

1. First, in a web browser:
    1. Go to [GitHub](https://github.com/jloughry?tab=repositories)'s list
of respositories and click the green 'New' button.
    1. Think of a subdirectory name (*new_name*) and fill in the
description.
    1. Leave it set to 'public' and don't tick the 'README' box (that and
the LICENSE file will be supplied from the template).
    1. Click the 'Create repository' button.
1. Next, on the local computer:
    1. `cd ~/thesis/github/`
    1. `git init new_name`
    1. `cd new_name`
    1. `cp -r ../new_paper/* .`
    1. `cp ../new_paper/.git/config ./.git/`
    1. Edit `.git/config` and change the name of the new directory (one
line).
    1. `cp ../new_paper/.gitignore .`
    1. Edit `.gitignore` and change the name of the PDF files (two lines).
    1. Put something reasonable in the `.git/description` file.
    1. Change the name of the target in `Makefile` to `new_name` (it should
match the name of the directory).
    1. `mv Journal_name_paper.tex new_name_paper.tex`
    1. `mv Journal_name_slides.tex new_name_slides.tex`
    1. `make` (see if it works)
    1. `make allclean`
    1. Update the README file.
    1. `make commit` (say 'initial commit')

(I really ought to turn this into a Makefile and use `sed` to make the
edits automatically.)

Git Usage Notes
---------------

A `make clean` is done automatically by the Makefile before committing. PDF
files are generally not stored; they are listed by name in the `.gitignore`
file.

