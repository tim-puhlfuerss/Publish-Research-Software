# 1. Create a Version-Controlled Repository

## TL;DR

- Version control prepares your project for sharing and collaboration.
- Include all relevant artifacts in the repository.
- Use a `.gitignore` file to exclude unnecessary files from version control.

## Why is This Process Important?

- Version control allows you to manage multiple project states and revert to previous states if needed.
- Git platforms enable artifact sharing and collaborative development.

## Prerequisites

First, check your organization's policies regarding the publication of software and data.
There may be specific obligations or restrictions.

## Where to Store the Code?

- Minimum: Local Git versioning system.
- Recommended: Backup on a collaboration platform such as:
  - GitHub
  - GitLab
  - BitBucket

## What Should be Part of the Public Repository?

- Everything required to create a usable version of the code and produce the intended results:
  - Code and data
  - Documentation (at least a `README.md` file)
  - Build scripts and configuration files (e.g., `requirements.txt`)
  - Test cases
  - (Example) input data
  - `.gitignore` file
    - To exclude unnecessary files and directories from version control and public sharing.
    - Use the [gitignore generator](https://www.toptal.com/developers/gitignore) by Toptal for a good starting configuration.

## What Should Not be Part of the Public Repository?

- Sensitive files and data, e.g., API keys or login information.
- Generated files, such as third-party libraries automatically downloaded during installation (e.g., `node_modules` in Node projects) or binary files generated during compilation.
- Large, static artifacts that could be published separately, such as datasets.

## What To Do With Large Data?

- Generic solutions:
  - [git-lfs](https://git-lfs.com) (large file storage; integrates with the standard Git workflow)
  - [git-annex](https://git-annex.branchable.com) (distributed storage with an adapted Git workflow)
  - These solutions help avoid automatically downloading large files when cloning the repository.
- Data analytics solutions:
  - [DVC](https://dvc.org) (distributed storage; workflow integrates an additional command line tool with Git)
  - [Datalad](https://handbook.datalad.org/en/latest/intro/executive_summary.html) (distributed storage; new command line tool instead of Git)
- Research artifact platforms:
  - [Zenodo](https://zenodo.org)
  - [Figshare](https://figshare.com)
  - You should reference the separately stored dataset in the Git repository.

## What To Do if Unwanted Information is Already Git-Versioned?

- Use [git filter-branch](https://git-scm.com/docs/git-filter-branch) to rewrite the Git history.
- Use [BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/) to remove large or sensitive data, like passwords.

## Further Reading

- [Version Control with Git tutorial](https://swcarpentry.github.io/git-novice/) by Software Carpentry
- [re3data](http://re3data.org/) to browse public research data repositories.
