# 1. Create a Version-Controlled Repository

## TL;DR

- Version control helps to prepare the code for sharing.
- Make sure to put all relevant artifacts into the repository.
- The `.gitignore` file helps to specify things you do not want to share.

## Why is This Process Important?

- Version control allows to browse multiple project states and enables to go back to a previous state if something went wrong during the development.
- Git platforms offer to share code and collaborate on it with others.

## Prerequisites

First step (if relevant): Check organizational policies for publishing software and data.
The organization or the project you work in might have obligations or restrictions for publishing research artifacts.

## Where to Store the Code?

- Minimum: Local Git versioning system
- Recommended: Backup on a collaboration platform, like:
  - GitHub
  - GitLab
  - BitBucket

## What Should be Part of the Repository?

- In general: Everything required to create a usable version of the code and produce the intended results.
- Code and data
- Documentation (at least a `README.md` file)
- Build scripts and configuration files (e.g., `requirements.txt`)
- Test cases
- (Example) input data
- `.gitignore` file
  - Enter names of files, file types, or entire directories that should not be version-controlled and shared publicly.
  - You can use the [gitignore generator](https://www.toptal.com/developers/gitignore) by Topal for a good start-up configuration.

## What Should not be Part of the Repository?

- Generated files, e.g., third-party libraries automatically downloaded during the installation process (e.g., `node_modules` folder in _Node_ projects) or binary files generated during the compilation process.
- Large, more static artifacts that could be published separately, e.g., datasets, databases.

## What To Do if Data is Too Large?

- Generic solutions:
  - [git-lfs](https://git-lfs.com) (large file storage; central storage, included in the standard Git workflow)
  - [git-annex](https://git-annex.branchable.com) (distributed storage with an adapted Git workflow)
  - These solution help avoiding to automatically download large files when cloning the repository
- Data analytics solutions:
  - [DVC](https://dvc.org) (distributed storage; workflow: additional command line tool + Git)
  - [Datalad](https://handbook.datalad.org/en/latest/intro/executive_summary.html) (distributed storage; workflow: new command line tool instead of Git)
- Research artifact platforms, e.g.:
  - [Zenodo](https://zenodo.org)
  - [Figshare](https://figshare.com)
- Reference the dataset in the Git repository.

## What To Do if Unwanted Information is Already Git-Versioned?

- [git filter-branch](https://git-scm.com/docs/git-filter-branch) to rewrite the Git history
- [BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/), e.g., to remove large data or sensible data, like passwords

## Further Reads

- [Version Control with Git tutorial](https://swcarpentry.github.io/git-novice/) by Software Carpentry
- [re3data](http://re3data.org/) to browse public research data repositories.
