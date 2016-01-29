Process
=======

Prioritizing and scheduling tasks 
---------------------------------

Scrum & Kanban
~~~~~~~~~~~~~~

TODO.

References:

-  http://leansoftwareengineering.com/ksse/scrum-ban/
-  http://www.infoq.com/minibooks/kanban-scrum-minibook

Bug tracking
~~~~~~~~~~~~

We use bug trackers to tracks bugs. Sometimes 

Of course the workflow is different when we work on customer projets and on open source projects.

One important thing to keep in mind is how to prioritize issues:

- Critical: TODO.
- Blocking: TODO.
- Major: TODO.
- Minor: TODO.


Tools
~~~~~

For our public projects, which are hosted on GitHub, we use GitHub's issue tracker.

We use Huboard as a kanban-like front-end to GitHub.

For our customers projets, we use Redmine (and ar considering switching to Taiga).


Git
---

Our git branching model is mix of `git-flow <http://nvie.com/posts/a-successful-git-branching-model/>`_ and `GitHub flow <http://scottchacon.com/2011/08/31/github-flow.html>`_.

- Anything in the master branch is deployable
- To work on something new, create a descriptively named branch off of master (ie: new-oauth2-scopes)
- Commit to that branch locally and regularly push your work to the same named branch on the server
- When you need feedback or help, or you think the branch is ready for merging, open a pull request
- After someone else has reviewed and signed off on the feature, you can merge it into master
- When making a release, we tag our tree with version numbers and make a branch from a release when we need to backport a patch.


Branching
~~~~~~~~~

TODO.

Code reviews
~~~~~~~~~~~~

TODO.

References
~~~~~~~~~~

- <http://www.stateofcode.com/2013/05/never-commit-to-master/>


Versionning and releasing
-------------------------

(Semantic) Versionning
~~~~~~~~~~~~~~~~~~~~~~

Releasing
~~~~~~~~~

To make a release:

- Update the following files: ``CHANGES.rst`` and ``CONTRIBUTORS.rst``.
- Test locally
- Commit and push, wait for CI server to report status.
- Tag: ``git tag vX.Y.Z``, then ``git push --tags``
- `make clean`
- Check source build: ``python setup.py sdist``
- Upload: ``python setup.py sdist upload``

When releasing a new package on PyPI, add the ``python setup.py register`` phase.

