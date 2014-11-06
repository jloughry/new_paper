Joe Loughry (joe.loughry@stx.ox.ac.uk)
===========

This is a *template* for a new journal paper; copy it and extend it.

How to Create a New Git Repository
----------------------------------

1. First, in a web browser:
    1. Go to [GitHub](https://github.com/jloughry?tab=repositories)'s list
of respositories and click the green 'New' button.
    1. Think of a subdirectory name (*new_name*) and fill in the
description.
    1. Leave it set to 'public' and don't tick the 'README' box (those will
be supplied from the template).
    1. Click the 'Create repository' button.
1. Next, on the local computer:
    1. `cd ~/thesis/github/`
    1. `git init new_name`
    1. `cd new_name`
    1. `cp ../new_paper/* .` NOTE: do **not** use `cp -r` here.
    1. `cp ../new_paper/.gitignore`
    1. Edit `.gitignore` and change the name of the PDF files.
    1. Edit `.git/config` and change the name of the new directory.
    1. Edit the `.git/description` file.
	1. `git add .`
	1. `git push origin master`

(I really ought to turn this into a Makefile and use `sed` to make the
edits automatically.)

Git Usage Notes
---------------

A `make clean` is done automatically by the Makefile before committing. PDF
files are generally not stored; they are listed by name in the `.gitignore`
file.

