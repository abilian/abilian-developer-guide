Python specific recommendations
===============================

Style guide & tools
-------------------

We're mostly following PEP8 and the `Google Python Style Guide <https://google.github.io/styleguide/pyguide.html>`_.

We've been using automated code checkers (mostly `Flake8 <http://flake8.pycqa.org/en/latest/>`_ nowadays) with appropriate settings to ensure that deviations from the coding standard, as well as some non-stylistic issues, are detected.

Furthermore, we're using `YAPF <https://github.com/google/yapf>`_ with the ``google`` settings, to automatically format our Python code. 

We're also using `isort <http://isort.readthedocs.io/en/stable/>`_ to sort imports according to semantic and cosmetic rules.  

We plan to use Git commit hooks to ensure that every new commit in the future fully respects these standards.

More:

- <https://github.com/amontalenti/elements-of-python-style>
- <https://github.com/marrow/marrow.github.io/wiki/Zen>


Python 2 vs. Python 3
---------------------

We're currently still using Python 2 in our production code.

From 2017 on, we plan to start new projects using only Python 3, unless there
are strong technical reasons not to do so.

We've started work to support Python 3 (alongside Python 2) on our open source
projects, using the "six" library. We plan to finish it in 2017.

We've used the `Python Future <http://python-future.org/>`_ project for this,
but more recently switched to `six <https://pythonhosted.org/six/>`_ because
it's more standard.

``pylint --py3k`` is quite useful to help identify issues in current Python 2
code preventing migration to Python 3.

More info:

- <https://docs.python.org/3/howto/pyporting.html>
- <http://python3porting.com/>
- <https://tech.yplanapp.com/2016/08/24/upgrading-to-python-3-with-zero-downtime/>
- <http://python-future.org/compatible_idioms.html>



General Python recommandations
------------------------------

- <http://stevenloria.com/python-best-practice-patterns-by-vladimir-keleshev-notes/>

TODO: add more.


Python tooling
--------------

In this section, we list tools that directly support our Python development process.

- YAPF (see above)
- Flake8 (see above)
- isort (see above)
- ``pip-tools`` (see below)
- Mypy (static checking using annotations)

Not used yet:

- Pylint (static checker, more powerful than Flake8 but needs more tuning). Currently used only to check for py3k compatibility (see above).


Managing dependencies
~~~~~~~~~~~~~~~~~~~~~

We manage dependencies for our projects and build them using pip.

Mandatory read: <https://caremad.io/2013/07/setup-vs-requirement/>.

Use pip-tools (<https://github.com/nvie/pip-tools>).


Virtualenv
~~~~~~~~~~

Virtualenv is a tool to create isolated Python environments.  Why is this good? You can create a new Python environment to run a Python/Flask/whatever app and install all package dependencies into the virtualenv without affecting your system’s site-packages. Need to upgrade a package to see how it affects your app? Create a new virtualenv, install/copy your app into it, run your tests, and delete it when you are done. Just like git makes branching inexpensive and easy, virtualenv makes creating and managing new Python environments inexpensive and easy.

The doc: <https://virtualenv.pypa.io/en/stable/>.

PyPI mirror
~~~~~~~~~~~

Note: as of early 2017, this is not true anymore.

We have set up an internal PyPI mirror, using the `devpi <http://doc.devpi.net/latest/>`_ project.

Its main use is for our CI server (Jenkins).

Of course, our public open source projects should be buildable without depending on it.


Packaging
~~~~~~~~~

We package our Python projects using the standard tools (distutils, setuptools, pip). 

The packaging allows us to distribute our modules for all developers who would like to use them.

The packages are hosted on Pypi mirror and can be installed with pip or easyinstall.

Standard structure for a Python project
---------------------------------------

A Python project MUST have the following files:

- ``README.rst``: we prefer ``.rst`` over ``.md`` because that's the markup language to use if you want your project to look good on PyPI.
- ``LICENSE.txt``
- ``setup.py`` and ``setup.cfg``
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
