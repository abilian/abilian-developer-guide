Development (and devops) tools and processes we are using
=========================================================

Here's a list of guidelines that are currently used. They are not set in
stone, of course, and will evolve as new techniques and methodologies
are explored by the team.


Build tools
-----------

Make
~~~~

We like having a Makefile at the root of our projects.

It should at least support the following targets:

- ``tests``
- ``clean`` and ``tidy``
- ``run``


Others
~~~~~~

As already stated elsewhere in this document, we're using `setuptools` to build Python packages.

For front-end packages, we're trying to catch up with the current best practices (which seem to change every 3 montsh or so).


Source code management
----------------------

We're using Git as our primary source code management system, and GitHub
as our main repository.

For public projects, we have a public project account
(https://github.com/abilian).

For private projects, I have a private personal account. We'll move to a
private group account later (it's more expensive ;).


Continuous integration
----------------------

We're using Travis for public projects, and a Jenkins instance for
private projects (+ for public projects too).

-  https://travis-ci.org/abilian/abilian-core (and other projects)
-  http://jenkins.abilian.com/


Tasks and issues management
---------------------------

We're currently using Redmine and Taiga.

This is not set in stone.


Devops tools
------------

Fabric
~~~~~~

Deployment to staging and production servers is currently managed by
Fabric using the Fabtools add-ons.

Later, we'll look into using Ansible or Salt, though at this point (for
single server deployment), I believe Fabric is the best choice.

Our Fabric scripts, however, are both a bit simplistic and convoluted.
For instance, they don't deal with database migration, code rollback,
etc.

Vagrant
~~~~~~~

We're using Vagrant to run full deployment tests on pristine virtual
machines. It should become most valuable when we will have actual
projects in production, and will need to address issues such as
upgrades.


Desktop tools
-------------

Editors and IDEs
~~~~~~~~~~~~~~~~

The best Python IDE is PyCharm, though its quality seems to be going down recently.

If you don't like IDEs, use a regular text editor, such as Emacs, Vim, Atom, Sublime... But make sure you have installed the plugins that will make you more productive, such as:

- Syntax highlighting
- Dynamic code linting
- Autocompletion


Chrome plugins
~~~~~~~~~~~~~~

Here are a few Chrome plugins that we find useful:

-  `BuildReactor <https://github.com/AdamNowotny/BuildReactor>`_: monitors CI builds
   (supports both Jenkins and Travis) and sends Growl-style
   notifications when a build fails.

-  `Check My Links <https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf>`_: link checker, useful when testing a web application.


Firefox plugins
~~~~~~~~~~~~~~~

- `Opcast Desktop <https://desktop.opquast.com/fr/>`_:  a Firefox extension that allows you to launch more than 450 tests (UX, SEO, accessibility, performance…) on the webpages you're currently browsing or coding.


Documentation
-------------

You probably want a tool on your laptop that gives you quick access to the documentation of the languages and libraries you are using.

On the Mac we're using `Dash <http://kapeli.com/dash>`_.

We've also found that printing "cheat sheets" can be useful.
