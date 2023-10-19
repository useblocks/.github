# Useblocks common practices

This document is intended to lay out some common best practices for useblocks repositories.
It is not intended to be followed to the letter, but rather to be a guideline for
maintainers to follow.

## License

All repositories should be licensed under the MIT license.

## Git Branches

Repositories should use the `main` branch as their primary branch.
This branch should be "protected" on GitHub and require PR reviews and status checks before merging (see [GitHub branch configuration](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule)).

Additions to the `main` branch should follow these simple concepts:

- Use feature branches for all new features and bug fixes.
- Merge feature branches into the `main` branch using pull requests.
- Keep a high quality, up-to-date `main` branch.

## Opening a Pull Request

Pull requests should be submitted to `main` early and often!

## Python repositories

- Use [poetry](https://python-poetry.org/) for dependency management.
- Use [pre-commit](https://pre-commit.com/) for code formatting and linting.
  - Use black for code formatting.
  - Use isort for import sorting.
  - Use ruff for linting.
- Use [mypy](https://mypy.readthedocs.io) for type checking, set to strict mode.
- Use [pytest](https://docs.pytest.org) for testing.

## Sphinx extensions

For repositories intended to provide sphinx extensions, the following should be
followed:

- The extensions should aim to support the latest THREE major versions of sphinx.
