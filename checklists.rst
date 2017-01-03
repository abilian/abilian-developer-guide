Important checklists
====================

Here we will list important checklists.

They are not written yet.


Committing
----------

Before a commit:

- TODO.


Releasing software packages
---------------------------

To release software (NB: TODO):

- Check that the following files are OK: README, INSTALL, CHANGELOG, CONTRIBUTORS
- Run tests locally
- Tag
- Build
- Push on PyPI

README checklist
~~~~~~~~~~~~~~~~

A helpful checklist to gauge how your README is coming along:

- One-liner explaining the purpose of the module
- Necessary background context & links
- Potentially unfamiliar terms link to informative sources
- Clear, runnable example of usage
- Installation instructions
- Extensive API documentation
- Performs cognitive funneling
- Caveats and limitations mentioned up-front
- Doesn't rely on images to relay critical information
- License

(From https://github.com/noffle/art-of-readme).


Scrum checklist
---------------

<https://www.crisp.se/wp-content/uploads/2012/05/Scrum-checklist.pdf>


Definition of Done
------------------

Definition: <http://guide.agilealliance.org/guide/definition-of-done.html>

See also: <http://www.scrum-breakfast.com/2014/05/the-three-faces-of-done.html>

Expected benefits:

- the Definition of Done provides a checklist which usefully guides pre-implementation activities: discussion, estimation, design
- the Definition of Done limits the cost of rework once a feature has been accepted as "done"
- having an explicit contract limits the risk of misunderstanding and conflict between the development team and the customer or product owner


For our open source projects, here is our definition (draft):

- Code produced (all ‘to do’ items in code completed)
- Code commented according to our commenting guidelines
- Code checked in in VCS, feature branch merged into development branch
- Peer reviewed (or produced with pair programming) and meeting development standards
- Builds without errors
- Quality check tools (linters) pass
- Unit tests written and passing
- Deployed to system test environment and passed system tests
- Demonstrated to product owner
- Any build/deployment/configuration changes implemented/documented/communicated
- Relevant documentation/diagrams produced and/or updated
- Release notes updated for upcoming release
- Ticket move to "Done" and/or closed

Other / misc checklists
-----------------------

- <http://webdevchecklist.com/> Web Developer Checklist
- <https://github.com/futurice/backend-best-practices#release-checklist>


