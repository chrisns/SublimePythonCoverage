``SublimePythonCoverage`` is a plugin for Sublime Text 3
that can highlight lines of Python lacking test coverage,
based on the output of Ned Batchelder's
`coverage.py <http://nedbatchelder.com/code/coverage/>`_.

Port from Sublime Text 2 plugin

https://github.com/davisagli/SublimePythonCoverage.git

Installation
------------

cd ~/.config/sublime-text-3/Packages
git clone https://github.com/zehome/SublimePythonCoverage.git

Usage
-----

Highlighting lines missing coverage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When you open a .py file,
SublimePythonCoverage tries to find coverage information
and mark all uncovered lines with a symbol in the gutter.

It does this by looking in all parent directories
until it finds a ``.coverage`` file as produced by ``coverage.py``.
Obviously, it only works if that file exists
and contains coverage information for the .py file you opened.

You can force a reload of the coverage information
and redraw of the outlines
by running the ``show_python_coverage`` command,
bound to super+shift+c by default.

Running tests with coverage
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Django
------

coverage run --source='' manage.py test
