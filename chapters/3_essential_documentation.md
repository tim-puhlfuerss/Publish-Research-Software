# 3. Add Essential Documentation

## TL;DR

- Provide documentation for potential users and contributors
- Add a `README` file as a minimum documentation artifact to your repository.

## Why is This Process Important?

- Good documentation can motivate and help:
  - Potential users to use your software.
  - Potential contributors to provide contributions efficiently.

## Target Groups and Their Information Needs

### Common Information Needs

- Problems which the software solves
- Overview of the software's main features
- Assumptions and constraints under which the software works
- Installation instructions (for multiple environments), including required dependencies
- Usage instructions (how to start the software, user manual)
- License under which the software can be used

### Users

- Easy availability and installation through package managers
- Basic examples for usage (example input and output data)
- API documentation (in case of libraries)
- Possibilities for support in case of problems
- Summary of changes in the software's behaviour
- Additionally for researchers:
  - Information and steps to reproduce results, incl. exact dependency version, operating system etc.
  - Citation information for the software

### Contributors

- Basic rules for issues, pull/merge requests and communication channels
- How to contribute bug fixes, changes, features
- Ground rules for communication behaviour and participation
- Technical information, e.g., architecture diagrams, typical solution patterns, extension points, and test instructions
- Code documentation: API and inline comments

## Typical Documentation Files

- `README` as repository entry point
  - Should describe all information needs mentioned above.
  - Should provide links to more specific documentation artifacts.
- `CONTRIBUTING` with the contribution guideline
- `CODE_OF_CONDUCT` with the ground rules for contributors' expected behaviour and participation
- `LICENSE` file with the license under which the entire project is provided, or a description of all (third-party) licenses in the `LICENSE` file and a `LICENSES` folder that lists all licenses.
- `CHANGELOG` that chronologically lists major changes.
- `CITATION` with information how to cite the software in scientific publication
- `ISSUE_TEMPLATE` and `PULL_REQUEST_TEMPLATE` folders with issue and pull request template files for contributors

## Typical Mark-up Languages for Documentation Files

- Markdown (see [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/))
- AsciiDoc (see [AsciiDoc Writer's Guide](https://asciidoctor.org/docs/asciidoc-writers-guide/))
- ReStructuredText (see [ReStructuredText tutorial for Sphinx](https://quick-sphinx-tutorial.readthedocs.io/en/latest/rst.html))
- Use [Pandoc](https://pandoc.org) to convert between the formats.

## Further Reads

- GitHub's [Community Profile](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-profiles-for-public-repositories)
- GitHub's [Open Source Guide](https://opensource.guide)
- Curated [Awesome README](https://github.com/matiassingers/awesome-readme) list
- [Standard README](https://github.com/RichardLitt/standard-readme) project
- [One-sentence-per-line principle](https://rhodesmill.org/brandon/2012/one-sentence-per-line/)
