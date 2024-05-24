# 1. Create a Version-Controlled Repository

## TL;DR

## Why is This Process Important?

First step (if relevant): Check organizational policies for publishing software and data.

## Code collaboration platforms

- GitHub
- GitLab
- BitBucket

## What should be part of the repository?

- Code and data
- Documentation (at least a `README.md` file)
- Build scripts and configuration files (e.g., `requirements.txt`)
- Test cases
- (Example) input data
- `.gitignore` file
  - Enter files, file types, or entire directories that should not be version-controlled and shared publicly.
  - You can use the [gitignore generator](https://www.toptal.com/developers/gitignore) by Topal for a good start-up configuration.

## What should not be part of the repository?

- Generated binary data (Git is weak in handling binary data)
- Third-party libraries (e.g., `node_modules` folder in Node-based projects)

## What to do if data is too large?

- Generic solutions:
  - [git-lfs](https://git-lfs.com) (large file storage; central storage that became a standard in the Git workflow)
  - [git-annex](https://git-annex.branchable.com) (distributed storage with an adapter Git workflow)
  - These solution help avoiding to automatically download large files when cloning the repository
- Data analytics solutions:
  - [DVC](https://dvc.org) (distributed storage; workflow: additional command line tool + Git)
  - [Datalad](https://handbook.datalad.org/en/latest/intro/executive_summary.html) (distributed storage; workflow: new command line tool instead of Git)
- Consider publishing large datasets separately:
  - e.g., Zenodo and Figshare
  - Reference the dataset in the Git repository

## What to do if unwanted information is already git-versioned?

- [git filter-branch](https://git-scm.com/docs/git-filter-branch) to rewrite the Git history
- [BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/), e.g., to remove large data or sensible data, like passwords
