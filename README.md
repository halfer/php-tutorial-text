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

The pages are held in a single file, using `__NEWFILE__` as a chapter separator. Menu titles are
derived from the first `<h2>` in each section, and small amounts of PHP are permitted. There are two
main uses for PHP in this repo: to render diffs and conditionally render non-live notes. Here's
how to render a tabbed (multi-file) diff block:

    <?php renderDiffFromComment('The comment text') ?>

Comments are used here, as hashes will break if changes are rebased in. In the unlikely event the
repo contains clashing comment texts, a simple date filter can be added.

Here's how to render a development mode note (the permitted note classes are `critical`, `todo`,
`in-progress` and `comment`):

	<?php if (showTodoMessages()): ?>
		<div class="todo note">
			Here's a note
		</div>
	<?php endif ?>

Once merged to this repo, pages are rebuilt manually by a script.

Notes:

- The single file format is fine for the moment, but if someone wants to see this split into
separate files, that can be arranged
- I'll add a code branch setting in this repo in due course, so multiple versions are supported. This
allows users in the middle of the tutorial to carry on reading the version they started with
- A good feedback loop for the text probably won't be initiated simply by making these repos public.
I suspect good commenting tools on the site itself will also be necessary
