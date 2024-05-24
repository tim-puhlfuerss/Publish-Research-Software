# 2. Create a Shareable State

## TL;DR

- Make sure others can install and (re-)use the software.
- Strive for comprehensible code.
- Do not share internals (sensitive information, absolute paths, local dependencies).

## Why is This Process Important?

- Others need to understand and reuse the artifacts.
- Mitigate security problems by removing sensitive information, e.g., API keys.

## General Hints

- Organize repository content with folders.
- Clearly state dependencies.
  - For Python:
    - Basic: Python version + `requirements.txt`
    - Advanced:
      - `requirements.in` file and `pip-compile` command
      - Python setuptools
      - Make file
      - Dev-based requirements (e.g., for testing) in a `requirements-extra.in` file
      - Check a [tutorial](https://medium.com/packagr/using-pip-compile-to-manage-dependencies-in-your-python-packages-8451b21a949e) on Medium.
  - Avoid dependencies with private resources (e.g., databases, libraries, servers).
- Convert absolute to relative paths.
- Remove / mask sensitive data, like passwords, API key, user accounts, internal IP addresses, etc.
- Add a shell script that helps users to automatically set up and start the project.
- Test the correctness and completeness of the installation process on a "clean machine".

## Improve the Code Style

- Check the guidelines of the programming language's or framework's user community.
- Read similar code of others to receive inspiration.
- Apply a standardized code style and use code linters and formatters within an IDE to apply the style consistently.
- Use code sanitizers to remove problematic code or configurations from the project.
- Use descriptive names for files, functions, etc.
- Use logical blocks to structure your code, e.g., functions.
- Add code comments to describe important aspects, such as the "bigger picture", or usage examples.
- Do not "over-comment" the code, especially with inline comments, as this can also hinder the readability.
- Apply pair-programming and code reviews (or least [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging)).

## Add Test Cases

- Automated tests work as an executable documentation for developers that want to reuse your code.
- Add small tests as early as possible, as a good starting point for an automated test pipeline.

## Further Reads

- [Guideline](https://www.bitecode.dev/p/relieving-your-python-packaging-pain) by Bite Code! how to avoid problems with Python package managers
