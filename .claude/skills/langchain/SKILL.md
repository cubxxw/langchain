```markdown
# langchain Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns, coding conventions, and workflows used in the `langchain` Python codebase. You'll learn how to structure files, write imports and exports, follow commit message conventions, and understand the project's approach to testing. This guide is ideal for contributors aiming to maintain consistency and quality in the codebase.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.py`, `dataProcessor.py`

### Import Style
- Use **relative imports** within modules.
  - Example:
    ```python
    from .utils import helper_function
    from ..models import ModelClass
    ```

### Export Style
- Use **named exports** (explicitly define what is exported).
  - Example:
    ```python
    __all__ = ["MyClass", "my_function"]
    ```

### Commit Messages
- Follow **conventional commit** patterns.
- Common prefixes: `ci`, `chore`
- Example:
  ```
  chore: update dependencies for security patch
  ci: add GitHub Actions workflow for testing
  ```

## Workflows

### Code Contribution
**Trigger:** When adding or updating code in the repository  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write code following camelCase file naming and relative imports.
3. Add or update named exports as needed.
4. Write or update tests in files matching `*.test.*`.
5. Commit changes using a conventional commit message (e.g., `chore: improve error handling`).
6. Push the branch and open a pull request.

### Dependency Update
**Trigger:** When dependencies need to be updated  
**Command:** `/update-deps`

1. Update the relevant dependency files (e.g., `requirements.txt`).
2. Run tests to ensure compatibility.
3. Commit with a message like `chore: update dependencies`.
4. Push and open a pull request.

### Continuous Integration
**Trigger:** When configuring or updating CI  
**Command:** `/setup-ci`

1. Add or modify CI configuration files as needed.
2. Use the `ci:` prefix in commit messages.
3. Test the workflow by pushing changes and verifying CI runs.

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `utils.test.py`).
- The specific testing framework is **unknown**, but tests should be placed in files matching the pattern.
- Example test file:
  ```python
  # utils.test.py

  from .utils import helper_function

  def test_helper_function():
      assert helper_function(2) == 4
  ```

## Commands
| Command        | Purpose                                         |
|----------------|-------------------------------------------------|
| /contribute    | Steps for contributing code                     |
| /update-deps   | Update project dependencies                     |
| /setup-ci      | Configure or update continuous integration      |
```
