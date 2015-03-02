Process
=======

Priorizing and scheduling tasks 
-------------------------------

Scrum & Kanban
~~~~~~~~~~~~~~

References:

-  http://leansoftwareengineering.com/ksse/scrum-ban/
-  http://www.infoq.com/minibooks/kanban-scrum-minibook


Git
---

Our git branchig model is mix of `git-flow <http://nvie.com/posts/a-successful-git-branching-model/>`_ and `GitHub flow <http://scottchacon.com/2011/08/31/github-flow.html>`_.

- Anything in the master branch is deployable
- To work on something new, create a descriptively named branch off of master (ie: new-oauth2-scopes)
- Commit to that branch locally and regularly push your work to the same named branch on the server
- When you need feedback or help, or you think the branch is ready for merging, open a pull request
- After someone else has reviewed and signed off on the feature, you can merge it into master
- When making a release, we tag our tree with version numbers and make a branch from a release when we need to backport a patch.


Branching
~~~~~~~~~

Code reviews
~~~~~~~~~~~~


Versionning and releasing
-------------------------

(Semantic) Versionning
~~~~~~~~~~~~~~~~~~~~~~

Releasing
~~~~~~~~~
