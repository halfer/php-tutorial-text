Tutorial text for "I ♥ PHP"
===

This repo contains the text for the "I ♥ PHP" tutorial.
The tutorial has been designed for beginner and improving-beginner programmers wishing to learn
some good practices in PHP web development. The code example uses PDO/SQLite, and demonstrates
parameterisation, HTML escaping, logic/content separation, authentication, form handling, sessions
and proper password hashing. The repo is public so that experienced developers may propose
improvements if they wish.

Code changes in the tutorial are shown as diffs in the text, and each modified file can be
downloaded in its entirety at that point of development. To facilitate this, files and diffs are
extracted from this repo by a script, rather than being copied in manually. This means that
code improvements are much easier to transpose to the tutorial, than the traditional method of
making adjustments by hand.

Here is [a blog post about the tutorial](http://blog.jondh.me.uk/2014/08/online-php-beginners-tutorial/),
which is presently in alpha status.

See also the [code repo here](https://github.com/halfer/php-tutorial-project).

Page build process
---

Notes:

- pages are built by a script
- diffs are looked up by commit message, so that rebases in the code repo doesn't break stuff
- in the unlikely event a commit message is not unique, I'll add a date filter
- I'll add a code branch setting in this repo in due course, so multiple versions are supported. This
allows users in the middle of the tutorial to carry on reading the version they started with
- A good feedback loop for the text probably won't be initiated simply by making these repos public.
I suspect good commenting tools on the site itself will also be necessary
