# 2. Create a Shareable State

## TL;DR

- Make sure others can install and (re-)use the project.
- Strive for comprehensible code.
- Do not share internals (sensitive information, absolute paths, local dependencies).

## Why is This Process Important?

- Otherwise, others might not be able to understand and reuse the artifact.
- Avoid sharing sensitive information, e.g., API keys

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
      - Tutorial on [Medium](https://medium.com/packagr/using-pip-compile-to-manage-dependencies-in-your-python-packages-8451b21a949e)  
  - Avoid dependencies on private resources (e.g., data, libraries, servers).
- Avoid absolute paths.
- Avoid sharing sensitive data, like passwords, API key, user accounts, internal IP addresses, etc.
- Add a shell script that helps users to automatically set up and start the project.
- Test the installation process on a "clean machine".

## Improve the Code Style

- Read similar code of others to receive inspiration.
- Check the guidelines of the programming language's or framework's user community.
- Apply a standardized code style and apply it consistently. Use code linters and formatters within an IDE to avoid inconsistencies.
- Use "sanitizers" to remove poor or problematic code or configuration from the project.
- Use descriptive names for files, functions, etc.
- Use logical blocks to structure your code, e.g., functions.
- Add code comments to describe important aspects, such as the "bigger picture", or usage examples.
- Do not "over-comment" the code, especially regarding inline comments, as this can also hinder the readability.
- Apply pair-programming and code reviews (or least [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging)).

## Add Test Cases

- Automated tests work as an executable documentation for developers that want to reuse your code.
- Add small tests as early as possible, as a good starting point for a CI/CD pipeline.
