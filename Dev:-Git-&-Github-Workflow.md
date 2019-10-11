# GITHUB GUIDELINES
## GIT FLOW
On GitHub, we use a practice commonly known as Git-Flow. You can read about the process in depth on [Vincent Driessen's Guide](https://nvie.com/posts/a-successful-git-branching-model/), off of which we base our current workflow. If at any point that guide conflicts with what is written here, the methods & instructions specified here should be used.

Familiarity with Git, specifically with using branches, is a must for interacting with Genten Studios' repositories and is a prerequisite for learning the Git-Flow process. The process is based on separating the project into categories of branches as follows: master, release, development, feature branches, and hotfixes.

**The Master Branch** is the *most* stable source for the code, this contains major/ minor releases and nothing else. Only release and hotfix branches can be pushed here.
- All Genten Developers and Staff Members must approve any push to the master branch - unless said otherwise (e.g. last minute hotfixes).
- The code must be thoroughly tested on all supported systems before being pushed here.

**Hot Fix Branches** are a method for pushing code to the master branch after a release. These should be minor fixes that add no functionality (unless the bug restricts a certain functionality) to the project.

**Release Branches** are the staging area for a release. Similar to a hotfix branch only bug testing is to be done here and no new features should be added. 
- A 3/4 developer approval to push to the release branch.
- The code must be tested on all supported systems before being pushed here.

**The Develop Branch** Is where new features are added, however not where they are worked on. Commits should be merged from a feature branch into the develop branch and from nowhere else.
- It takes a greater than 2/3 developer approval to push to the develop branch.
- The code must be tested on all supported systems before being pushed here.

**Feature Branches** are where the action happens, each feature branch contains the addition of a single new feature. This is where all main development work happens and it is required to create a feature branch to push code. Any Genten developer can accept code into a feature branch.
- These branches must follow the naming convention of ``feat-[Component]-[feature name]`` (e.g. ``feat-rendering-api``)
PULL REQUESTS
- A pull request from a contributors repository can be approved by a single developer, this code can only be pulled into feature branches and not directly into the development or higher branches.
MERGE CHECKLIST
- This section lists the requirements for merging code. All of these requirements must be satisfied before code is merged into any branch.

## PR checklist
All Branches:
- Accomplish the feature(s) it was designed to accomplish
- Has the branch it's merging into merged onto itself and all conflicts are resolved
- Clean of all binaries and other non-source material
- Code is documented
- Complies with style guide
- All Developer reviewer comments are resolved
- Code is formatted with cLang

Development branch:
- Compiles properly on all supported systems

## VERSIONING AND RELEASES
Versioning will follow a standard of MAJOR.MINOR.FIX where Major Releases mark significant points in a product’s lifetime and Minor Releases mark the finalization of significant features. Fixes and non-feature releases are ones that repair issues with code.

Each project will have a drafted project plan/roadmap that marks each Major and Minor release scheduled in advance throughout the development life cycle.

Each project moves to an Alpha state when it is ready for community contributions, then a beta state when it is ready for playtesting. These states do not have to correspond to a specific version number but should occur before 1.0 during a Minor Release. Each project will reach a released state at 1.0, this is where the product is ready to be played regularly.
