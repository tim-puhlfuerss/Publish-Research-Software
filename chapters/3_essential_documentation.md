# 3. Add Essential Documentation

## TL;DR

- Provide comprehensive documentation for potential users and contributors.
- As a minimum, include a `README` file in your repository.

## Why is This Process Important?

- Good documentation:
  - Encourages potential **users** to adopt your software.
  - Helps potential **contributors** make effective contributions.

## Target Groups and Their Information Needs

### Common Information Needs

- Problems the software solves
- Overview of the software's main features
- Assumptions and constraints of the software
- Installation instructions for multiple environments, including required dependencies
- Usage instructions, including how to start the software and a user manual
- License information

### Users

- Easy availability and installation through package managers
- Basic usage examples, including example input and output data
- API documentation
- Support options for troubleshooting
- Summary of changes in software behavior
- For researchers:
  - Steps to reproduce results, including exact dependency versions and operating system details
  - Citation information for the software

### Contributors

- Guidelines for issues, pull/merge requests, and communication channels
- Instructions for contributing bug fixes, changes, and features
- Rules for communication behavior and participation
- Technical information, including architecture diagrams, typical solution patterns, extension points, and test instructions
- Code documentation, such as API details and inline comments

## Typical Documentation Files

- `README`: The entry point for the repository that should address all common information needs and link to more specific documentation artifacts.
- `CONTRIBUTING`: Guidelines for contributions
- `CODE_OF_CONDUCT`: Ground rules for contributor behavior and participation
- `LICENSE`: The project's license or descriptions of all third-party licenses, potentially accompanied by a `LICENSES` folder listing all licenses.
- `CHANGELOG`: A chronological list of major changes
- `CITATION`: Information on how to cite the software in scientific publications
- `ISSUE_TEMPLATE` and `PULL_REQUEST_TEMPLATE`: Templates for contributors to use when creating issues and pull requests

## Typical Markup Languages for Documentation Files

- **Markdown**: See the [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)
- **AsciiDoc**: Refer to the [AsciiDoc Writer's Guide](https://asciidoctor.org/docs/asciidoc-writers-guide/)
- **ReStructuredText**: See the [ReStructuredText tutorial for Sphinx](https://quick-sphinx-tutorial.readthedocs.io/en/latest/rst.html)
- **Pandoc**: Use [Pandoc](https://pandoc.org) to convert between different markup formats.

## Further Reading

- GitHub's [Community Profile](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-profiles-for-public-repositories)
- GitHub's [Open Source Guide](https://opensource.guide)
- Curated [Awesome README](https://github.com/matiassingers/awesome-readme) list
- [Standard README](https://github.com/RichardLitt/standard-readme) project
- The [One-sentence-per-line principle](https://rhodesmill.org/brandon/2012/one-sentence-per-line/)
