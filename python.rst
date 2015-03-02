Python specific recommendations
===============================

Style guide
-----------

We're mostly following PEP8 and the Google Python Style Guide (<http://google-styleguide.googlecode.com/svn/trunk/pyguide.html>).

The major deviation is that we prefer our indentation to be 2 spaces instead of 4.

I have tried the three main code checkers out there (pep8, PyFlakes and PyLint) but haven't found them very useful, except to track trivial issues.


Python 2 vs. Python 3
---------------------

We're currently still using Python 2.

We've started work to support Python 3 (alongside Python 2) on our open source projects, we plan to finish it in 2015.

We're using the `Python Future <http://python-future.org/>`_ project for this. 

This cheat sheet: <http://python-future.org/compatible_idioms.html> is specially usful.


General Python recommandations
------------------------------

- <http://stevenloria.com/python-best-practice-patterns-by-vladimir-keleshev-notes/>


Python tooling
--------------

In this section, we list tools that directly support our Python development process.


Managing dependencies
~~~~~~~~~~~~~~~~~~~~~

We manage dependencies for our projects and build them using pip.

Mandatory read: <https://caremad.io/2013/07/setup-vs-requirement/>.


Virtualenv
~~~~~~~~~~


PyPI mirror
~~~~~~~~~~~

We have set up a PyPI mirror, using the `devpi <http://doc.devpi.net/latest/>`_ project.

Its main use is for our CI server (Jenkins).

Of course, our public open source projects should be buildable without dependencies on it.


Packaging
~~~~~~~~~

We package our Python projects using



Additional Python links
-----------------------

These documents are rich collections of tips and links to sources of knowledge:

- <http://docs.python-guide.org/>
- <http://www.fullstackpython.com/table-of-contents.html>
- <https://github.com/kirang89/pycrumbs/blob/master/pycrumbs.md>
