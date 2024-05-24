# 6. Release the Repository

## TL;DR

- Mark software versions as releases using release numbers and tags.
- Document important changes in a changelog.
- Archive the release packages.

## Why is This Process Important?

- Otherwise, users do not know which version is considered stable.
- Otherwise, users do not know which version has been used to produce a specific result.
- You are able to easier start investigating problems that a user had with your code.

## Release Basics

- A __release__ is a specific working version of your software which you used, e.g., to produce specific research results.
- A __release number__ uniquely identifies a specific released software version.
- There are different release number schemes; examples:
  - [Semantic Versioning](https://semver.org) (e.g., `1.0.1`)
  - [Calendar Versioning](https://calver.org) (e.g., `2021-04-22`).
- A [__release tag__](https://git-scm.com/book/en/v2/Git-Basics-Tagging) is used to mark a specific released software version in the repository.
It should be named in accordance to the release number to ensure that it can be easily found if needed.
- A [__changelog__](https://keepachangelog.com/en/1.1.0/) documents all released versions of the software, including major changes of these versions.
It is written from the user's point of view.
Consider to [(semi-)automate updating the changelog](https://dev.to/devsatasurion/automate-changelogs-to-ease-your-release-282).
- A __release package__ can be used by a user to directly install and use a released software version.
  - It contains the software (e.g., source code, compiled executable), including proper user documentation (e.g., install and usage instructions, license information, citation information).
  - In the simplest form, it might be a snapshot of your source code repository packaged as ZIP file.
  Details depend on your programming language and target audience.
  - For a standalone software tool, you would consider publishing it on a code distribution platform, such as [PyPi](https://pypi.org), [CRAN](https://cran.r-project.org), or [MVN](https://mvnrepository.com).
  On this basis, users can easily install and use it via their typically used package manager.

## Minimal Release Checklist for Research Code

1. Before you start, make sure that you:
   - Defined the release number scheme.
   - Established the name mapping between release number and release tags.
   - Defined how to handle citation metadata.
   - Defined where you want to archive the code.
   - Defined the format and content of the release packages.

2. Prepare code for release
   - Define the release number for the release.
   - Document the user-visible changes in the changelog.
   - Update the citation metadata for this release.

3. Check code
   - Make sure that the code fulfills its intended functionality in the environments for which the code should work.
   - It is recommended to automate some checks by using automated tests and linting.
   - Review the documentation.

4. Publish and archive the release
   - Mark the release in the source code repository using a tag.
   This step ensures that one can easily identify the content of the released version in the source code repository.
   - Create the release package and eventually publish it on a code distribution platform.
   - Archive the release package.
