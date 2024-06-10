# 2. Create a Shareable State

## TL;DR

- Ensure others can install and (re-)use your software.
- Strive for comprehensible and clean code.
- Avoid sharing sensitive information, absolute paths, and local dependencies.

## Why is This Process Important?

- Others need to understand and reuse your artifacts.
- Removing sensitive information mitigates security risks, such as exposed API keys.

## General Hints

- **Organize Repository Content**: Use folders to structure your repository logically.
- **State Dependencies Clearly**:
  - For Python:
    - **Basic**: Specify the Python version and include a `requirements.txt` file.
    - **Advanced**:
      - Use a `requirements.in` file and the `pip-compile` command.
      - Utilize Python setuptools.
      - Create a Makefile.
      - Include development dependencies (e.g., for testing) in a `requirements-extra.in` file.
      - Refer to [this tutorial](https://medium.com/packagr/using-pip-compile-to-manage-dependencies-in-your-python-packages-8451b21a949e) for more details.
  - **Avoid Private Resources**: Do not rely on private databases, libraries, or servers.
- **Convert Absolute Paths to Relative Paths**: Ensure paths are relative to the project directory.
- **Remove or Mask Sensitive Data**: Exclude passwords, API keys, user accounts, internal IP addresses, etc.
- **Provide Setup Scripts**: Include a shell script to help users set up and start the project automatically.
- **Test Installation on a Clean Machine**: Verify the installation process on a system that mimics a new user environment.

## Improve the Code Style

- **Follow Community Guidelines**: Adhere to the coding standards of the language or framework you are using.
- **Learn from Others**: Read similar code from other projects for inspiration.
- **Use Standardized Code Style**: Apply consistent coding conventions with the help of linters and formatters in your IDE.
- **Use Code Sanitizers**: Remove problematic code or configurations.
- **Descriptive Naming**: Name files, functions, and variables descriptively.
- **Logical Code Structure**: Organize your code into logical blocks, such as functions and modules.
- **Comment Wisely**: Add comments to explain important aspects and provide usage examples, but avoid excessive inline comments that can hinder readability.
- **Collaborate**: Engage in pair programming and code reviews.
If that's not possible, use techniques like [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging).

## Add Test Cases

- **Automated Tests**: These serve as executable documentation, helping developers understand how to use your code.
- **Start Small**: Add basic tests early, laying the foundation for an automated test pipeline.

## Further Reading

- [Relieving Your Python Packaging Pain](https://www.bitecode.dev/p/relieving-your-python-packaging-pain) by Bite Code!: A guide to avoid problems with Python package managers.
