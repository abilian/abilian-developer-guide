Python specific recommendations
===============================

Style guide
-----------

We're mostly following PEP8 and the `Google Python Style Guide <http://google-styleguide.googlecode.com/svn/trunk/pyguide.html>`_.

The major deviation is that we prefer our indentation to be 2 spaces instead of 4. This may change in the future.

We've been using automated code checkers (pep8, PyFlakes and PyLint) with appropriate settings to ensure that deviations from the coding standard, as well as some non-stylistic issues, are detected.

We plan to use Git commit hooks to ensure that every new commit in the future fully respects these standards.

More:

- <https://github.com/amontalenti/elements-of-python-style>


Python 2 vs. Python 3
---------------------

We're currently still using Python 2.

We've started work to support Python 3 (alongside Python 2) on our open source projects, we plan to finish it in 2015.

We're using the `Python Future <http://python-future.org/>`_ project for this. 

This `cheat sheet <http://python-future.org/compatible_idioms.html>`_ is specially useful.


General Python recommandations
------------------------------

- <http://stevenloria.com/python-best-practice-patterns-by-vladimir-keleshev-notes/>

TODO: add more.


Python tooling
--------------

In this section, we list tools that directly support our Python development process.


Managing dependencies
~~~~~~~~~~~~~~~~~~~~~

We manage dependencies for our projects and build them using pip.

Mandatory read: <https://caremad.io/2013/07/setup-vs-requirement/>.


Virtualenv
~~~~~~~~~~

TODO.

PyPI mirror
~~~~~~~~~~~

We have set up an internal PyPI mirror, using the `devpi <http://doc.devpi.net/latest/>`_ project.

Its main use is for our CI server (Jenkins).

Of course, our public open source projects should be buildable without depending on it.


Packaging
~~~~~~~~~

We package our Python projects using the standard tools (distutils, setuptools, pip). 

TODO.


Standard structure for a Python project
---------------------------------------

A Python project MUST have the following files:

- ``README.rst``: we prefer ``.rst`` over ``.md`` because that's the markup language to use if you want your project to look good on PyPI.
- ``LICENSE.txt``
- ``setup.py``
- ``requirements.txt``
- ``tox.ini`` 
- ``.travis.yml``
- ``Makefile``: cf. supra.

It SHOULD also have the following files:

- ``setup.cfg``: used to contain config for additional files (ex: Babel, pep8, pyflakes, Sphinx...)
- ``etc/``: containing additional configuration files for tools that don't support ``setup.cfg`` (ex: ``pylint.rc``).

It MAY also contain:

- ``Vagrantfile``
- ``Dockerfile``
- ``deploy/``: for scripts related to deployment (bash, Ansible...)
- ``fabfile.py``: same


Additional Python links
-----------------------

These documents are rich collections of tips and links to sources of knowledge:

- <http://docs.python-guide.org/>
- <http://www.fullstackpython.com/table-of-contents.html>
- <https://github.com/kirang89/pycrumbs/blob/master/pycrumbs.md>
