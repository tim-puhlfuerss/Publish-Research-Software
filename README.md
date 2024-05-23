# How to Publish Research Software

Notes based on the course ["Foundation of Research Software Publication"](https://events.hifis.net/event/1344/overview) by the [Helmholtz Information and Data Science Academy (HIDA)](https://www.helmholtz-hida.de/) on 2024/05/23 and /24.

Original course material is available via [Git](https://codebase.helmholtz.cloud/hifis/software/education/hifis-workshops/foundations-of-research-software-publication/workshop-materials) and [HedgeDoc](https://notes.desy.de/rVHUTRVsTR2qVTiXjrDHCg?view).

## TL;DR

How should I publish my research-related code (and data) to enable others to check, reproduce, or reuse my results?

1. Put the results in a version-controlled repository
2. Create a shareable state
3. Add essential documentation
4. Add a license
5. Make the code citable
6. Release the repository

## 1. Create a Version-Controlled Repository

First step (if relevant): Check organizational policies for publishing software and data.

### Code collaboration platforms

- GitHub
- GitLab
- BitBucket

### What should be part of the repository?

- Code and data
- Documentation (at least a `README.md` file)
- Build scripts and configuration files (e.g., `requirements.txt`)
- Test cases
- (Example) input data
- `.gitignore` file
  - Enter files, file types, or entire directories that should not be version-controlled and shared publicly.
  - You can use the [gitignore generator](https://www.toptal.com/developers/gitignore) by Topal for a good start-up configuration.

### What should not be part of the repository?

- Generated binary data (Git is weak in handling binary data)
- Third-party libraries (e.g., `node_modules` folder in Node-based projects)

### What to do if data is too large?

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

### What to do if unwanted information is already git-versioned?

- [git filter-branch](https://git-scm.com/docs/git-filter-branch) to rewrite the Git history
- [BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/), e.g., to remove large data or sensible data, like passwords

## 2. Create a Shareable State

### General Hints

- Organize repository content with folders.
- Clearly state dependencies.
  - For Python:
    - Basic: Python version + `requirements.txt`
    - Advanced:
      - `requirements.in` file and `pip-compile` command
      - Python setuptools
      - Make file
      - Dev-based requirements (e.g., for testing) in a `requirements-extra.in` file
      - Tutorial on [Medium](https://medium.com/packagr/using-pip-compile-to-manage-dependencies-in-your-python-packages-8451b21a949e)  
  - Avoid dependencies on private resources (e.g., data, libraries, servers).
- Avoid absolute paths.
- Avoid sharing sensitive data, like passwords, API key, user accounts, internal IP addresses, etc.
- Check the guidelines of the programming language's or framework's user community.
- Apply pair-programming and code reviews (or least [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging)).
- Add a shell script that helps users to automatically set up and start the project.

### Improve the Code Style

- Apply a standardized code style consistently. Use code linters to avoid inconsistencies.
- Use self-explaining names
- Do not overcomment the code
- Use code checkers to sanitize the project from poor or problematic code

### Add Test Cases

- Automated tests work as an executable documentation for developers that want to reuse your code.
- Add small tests as early as possible, as a good starting point for a CI/CD pipeline.

## 3. Add Essential Documentation

Mind your audience and create documentation occording to at least the following perspectives:

- Users of the software/data
- Contributors that can help improving the repository

### Typical Documentation Files

- `README.md` as entry point to the repository with the following information:
  - Short description of the repository (What? Why?)
  - Installation and configuration instructions
  - Usage instructions
  - Test instructions
  - Project/code architecture details
  - Link to changelog + eventually info about latest update
  - Link to contribution guidelines
  - Link to code of conduct
  - Link to license
  - Citation information
- `CONTRIBUTING`
- `CODE_OF_CONDUCT`
- `LICENSE` file or `LICENSES` folder
- `CHANGELOG`
- `ISSUE_TEMPLATE` and `PULL_REQUEST_TEMPLATE` folders with issue and pull request template files

### Typical Mark-up Languages

- Markdown (see [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/))
- AsciiDoc (see [AsciiDoc Writer's Guide](https://asciidoctor.org/docs/asciidoc-writers-guide/))
- ReStructuredText (see [ReStructuredText tutorial for Sphinx](https://quick-sphinx-tutorial.readthedocs.io/en/latest/rst.html))
- Use [Pandoc](https://pandoc.org) to convert between the formats

### Further Information About Open Source Documentation

- GitHub's [Community Profile](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-profiles-for-public-repositories)
- GitHub's [Open Source Guide](https://opensource.guide)
- Curated [Awesome README](https://github.com/matiassingers/awesome-readme) list
- [One-sentence-per-line principle](https://rhodesmill.org/brandon/2012/one-sentence-per-line/)
