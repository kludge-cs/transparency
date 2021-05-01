# Repository Management System

## Abstract

This document details how we handle our version control system repositories at
Kludge Cyber Systems. We use Git as opposed to Mercurial because of the better
performance (patches vs diff streams), more effective branching structure
(commit line references vs consecutive changesets), et cetera.

## Branching

Kludge Cyber Systems makes use of the following branch architecture.
```
main    -*-*-*-*-*-*-
staging  `-*-*-*-*-'
t*/*       `-*-*-'
```
(`t*` represents a commit type under the Angular convention, and `*` represents
a hyphenated brief ASCII summary of the changes)

**Note**: The staging branch is optional, depending on the release cycle of the
project. If the staging branch is in use, it is used for change aggregation and
pre-releases. If it is not, the release cycle resolves solely around primary
releases on main. This is done to allow pre-release testing as well as better
control over releases for larger projects.

### Merging - Rejoining History

The protocol for merging into main is as follows:

1. Ensure all CI checks have passed
2. Ensure there are no remaining unresolved reviews or requested changes
3. Ensure all code owner reviews have been completed
4. Ensure there are at least two approvals

The protocol for merging into staging is as follows:

1. Ensure all CI checks have passed
2. Ensure there are no remaining unresolved reviews or requested changes

For either of the above protocols, if all of the above are true, you may tag the
pull request with the `status: merge-ready` label. Mergify will then handle
rebasing the pull request atop the target branch and merge for you.

## Continuous Integration

At Kludge Cyber Systems, we have opted to use Concourse CI instead of GitHub
Actions for most projects. This is due to the fact that Concourse workflows can
be tested locally with ease using Docker, whereas GitHub Actions typically
require several re-commits to test properly.

We use GitHub Actions exclusively for things such as automatic labelling and
workflows that would not be possible without it, such as our own
`gitcord-release-changelogger`.

The mandatory workflows for each project are as follows:
- Unit testing for all applicable platforms and versions
- Linting
- Integrations such as LGTM
- Our automatic labelling, and workflows bundled with [kludge-cs/.github]

[kludge-cs/.github]: https://github.com/kludge-cs/.github
