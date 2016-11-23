# How to contribute

This is a private Git repository and only esure's Digital Apps team is permitted to change this Digital App. If you have any suggestions or if you find an issue then please contact the team. Please see [AUTHORS.md](AUTHORS.md) for details of the team.


## The Agile Approach

esure uses an Agile methodology to track all of its Digital App changes, with each change communicated as an 'Agile Story'. All stories within a Sprint must pass through the following 'life cycle' phases:
| To Do | In Progress | Review | Complete |
| Stories waiting to be started. | Stories currently being worked on by a team member. | Stories ready to be reviewed by another team member. | Stories considered complete. |
The status of each story is captured and displayed on a project team's Kanban board.


## Branching

To ensure that our coding practices support esure's Agile approach we have adopted a branching strategy based on **Git-Flow**, aligning the Git-Flow steps with a stories life cycle. It is recommended that you familiarize yourself with Git-Flow before proceeding.

![Branching Strategy Image](/_docs/imgs/DevFlow@1x.png "Digital Apps Branching Strategy")

This branching strategy uses GitHub as the communication hub for all developers. Developers work locally and push branches to the central repository.

### Historical Branches

Instead of a single master branch, our branching strategy uses two branches to record the history of the project. The `master` branch stores the official release history, and the `develop` branch serves as an integration branch for features. It’s also convenient to tag all commits in the master branch with a version number.

### Feature (Story) Branches

Each new Agile story should reside in its own feature branch, which can be pushed to the central repository for peer review/collaboration. But, instead of branching off of `master`, feature branches use develop as their parent branch. When a feature is complete, it gets merged back into `develop`. Features should never interact directly with `master`.


**Pull Requests and Peer Reviews**

Before a feature is merged into `develop` a Pull Request should be opened allowing other developers and/or the technical team lead to review and approver the changes, with all issues and comments recorded on the GitHub platform. The [PEER_REVIEW.md](PEER_REVIEW.md) checklist should be used to help with this process.
Please ensure that all automated coding standard tests have been successfully executed and the evidence is available before submitting a Pull Request. This will make the peer review process quicker.

**Best Practices**:

* May branch off: `develop`
* Quality Assurance: Branch comments include evidence of peer review sign off.
* Must merge back into: `develop`
* Branch naming convention: anything except `master`, `develop`, `release-*`, or `hotfix-*`

### Release Branches

Once `develop` has acquired enough features for a release (or a scheduled Sprint release date is approaching), you fork a release branch off of `develop`.

Creating this branch starts the next release cycle, so no new features can be added after this point-only bug fixes, documentation generation, and other release-oriented tasks should go in this branch.

Once it’s ready to go into production, the release gets merged into `master` and tagged with a version number. In addition, it should be merged back into `develop`, which may have progressed since the release was initiated.

This approach creates well-defined phases of development and release.

**Best Practices:**

May branch off: `develop`
Must merge back into: `develop` and `master`
Tag: increment `major` or `minor` number
Branch naming convention: `release-*`

### Hotfix Branches

“Hotfix” branches are used to quickly patch production releases. This is the only branch that should fork directly off of `master`. As soon as the fix is complete, it should be merged into both `master` and `develop` (or the current `release` branch), and `master` should be tagged with an updated version number.

This approach should only be considered for critical maintenance issues.

**Best Practices:**

May branch off: `master`
Must merge back into: `master` and `develop`
Tag: increment `hotfix` number
Branch naming convention: `hotfix-*`


## Tools

The following suite of tools has been used to develop this Digital App. It's recommended that all contributers use the same tools to help reduce formating conflicts.

* Project Management: [JIRA](https://myesure.atlassian.com/), 
* Project Documentation: [Confluence](https://myesure.atlassian.com/), 
* Graphical: [Sketch](https://www.sketchapp.com),
* Development:
* Testing:


