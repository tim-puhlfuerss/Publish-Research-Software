# 6. Release the Repository

## TL;DR

- Mark software versions as releases using release numbers and tags.
- Document important changes in a changelog.
- Archive the release packages.

## Why is This Process Important?

- Users can identify which version is considered stable.
- Users get to know which version you used to produce specific results.
- Users can report problems related to a specific software version.

## Release Basics

- A **release** is a specific, stable version of your software used for producing research results.
- A **release number** uniquely identifies each released version.
- Common release numbering schemes:
  - [Semantic Versioning](https://semver.org) (e.g., `1.0.1`)
  - [Calendar Versioning](https://calver.org) (e.g., `2021-04-22`)
- A [**release tag**](https://git-scm.com/book/en/v2/Git-Basics-Tagging) is a marker in the repository corresponding to the release number, making it easy to find the specific version.
- A [**changelog**](https://keepachangelog.com/en/1.1.0/) documents all released versions and their major changes from the user’s perspective.
Consider [semi-automating the updating of the changelog]((https://dev.to/devsatasurion/automate-changelogs-to-ease-your-release-282)).
- A **release package** includes the software (raw source code and/or compiled executable) and proper documentation, such as installation instructions, usage instructions, license information, and citation information.
This can be a ZIP file or published on platforms like [PyPi](https://pypi.org), [CRAN](https://cran.r-project.org), or [MVN](https://mvnrepository.com) for easier user access.

## Minimal Release Checklist for Research Code

### 1. Before You Start

- Define the release number scheme.
- Establish the name mapping between release numbers and release tags.
- Determine how to handle citation metadata.
- Decide where to archive the code.
- Define the format and content of release packages.

### 2. Prepare Code for Release

- Define the release number for the release.
- Document user-visible changes in the changelog.
- Update the citation metadata for this release.

### 3. Check the Code

- Ensure the code fulfills its intended functionality in the target environments.
- Automate checks using tests and linting to catch bugs early.
- Review the documentation.

### 4. Publish and Archive the Release

- Mark the release in the source code repository with a tag to identify the released version.
- Create and publish the release package, potentially on a code distribution platform.
- Archive the release package, e.g., on Zenodo, to receive a persistent identifier.
