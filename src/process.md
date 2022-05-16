# Process

## Prioritizing and scheduling tasks

### Scrum & Kanban

TODO.

References:

- <http://leansoftwareengineering.com/ksse/scrum-ban/>
- <http://www.infoq.com/minibooks/kanban-scrum-minibook>

### Bug tracking

We use bug trackers to tracks bugs.

Of course the workflow is different when we work on customer projets and on open source projects.

One important thing to keep in mind is how to prioritize issues. For this, we're roughly following the *IEEE Standard Classification for Software Anomalies*:

- **Blocking**: Testing is inhibited or suspended pending correction or identification of suitable workaround.
- **Critical**: Essential operations are unavoidably disrupted, safety is jeopardized, and security is compromised.
- **Major**: Essential operations are affected but can proceed.
- **Minor**: Nonessential operations are disrupted.
- **Inconsequential**: No significant impact on operations.

### Tools

For both our public projects and our internal communication, we're using GitHub's issue tracker and GitHub "Projects" (kanban-style vue on issues and pull requests).

When we need to communicate (privately) with our customers, we're using (currently) either Redmine (private instance) or Trello.

## Git

### Branch model

There are basically two main branching models for git-based development:

- [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) or its close cousin [GitHub flow](http://scottchacon.com/2011/08/31/github-flow.html).
- [Trunk based developmen](https://trunkbaseddevelopment.com/).

Wether we use the former or the latter depends on several factors, some of which are contextual.

Here are a few principles:

- Anything in the trunk (also called "main") branch is deployable.
- Ensure that the code you work on is thouroughly tested (~100% coverage)
- **Either**: commit improvement directly to trunk, and count on a posteriori code reviews to ensure ("better ask forgiveness than permission")
- **Or**:
  : - To work on something new, create a descriptively named branch off of master (ie: new-oauth2-scopes)
    - Commit to that branch locally and regularly push your work to the same named branch on the server
    - When you need feedback or help, or you think the branch is ready for merging, open a pull request
    - After someone else has reviewed and signed off on the feature, you can merge it into master
- When making a release, we tag our tree with version numbers and make a branch from a release when we need to backport a patch.

### Commit messages

Prefix each commit with one of the following:

- feat: A new feature
- fix: A bug fix
- docs: Documentation only changes
- style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- refactor: A code change that neither fixes a bug nor adds a feature
- perf: A code change that improves performance
- test: Adding missing or correcting existing tests
- chore: Changes to the build process or auxiliary tools and libraries such as documentation generation

See:

- Use [Conventional Style](https://www.conventionalcommits.org/en/v1.0.0/) to format your commit messages.
- Use [Auto-Changelog](https://github.com/KeNaCo/auto-changelog) to generate Changelogs from commit messages.
- Some additional remarks on [Commit messages:](https://github.com/RomuloOliveira/commit-messages-guide).
- See also: <https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#commits>

### Code reviews

See: \<<https://blog.scottnonnenberg.com/top-ten-pull-request-review-mistakes/>>.

## Versionning and releasing

### (Semantic) Versionning

See:

- \<<http://semver.org/>>
- \<<https://www.python.org/dev/peps/pep-0440/>>
- \<<https://github.com/relekang/python-semantic-release>>

### Releasing

We're (currently) using the [setuptools-scm](https://github.com/pypa/setuptools_scm) package to define version numbers for packages from git tags.

To make a release using this system:

- Update the following files: `CHANGES.rst` and `CONTRIBUTORS.rst`.
- Test locally
- Commit and push, wait for CI server to report status.
- Tag: `git tag vX.Y.Z`, then `git push --tags`
- `make clean`
- Check source build: `python setup.py sdist`
- Upload: `python setup.py sdist upload`

When releasing a new package on PyPI, add the `python setup.py register` phase.

This may change in the future.
