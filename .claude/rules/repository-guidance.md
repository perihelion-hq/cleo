# Repository guidance

- Follow [CONTRIBUTING.md](../../CONTRIBUTING.md) for Poetry setup, test and pre-commit checks, and news-fragment requirements; keep that document as the owner of the contribution procedure.
- Include type checking when validating Python changes: CI has both type-checking and test steps (see [.github/workflows/tests.yaml](../../.github/workflows/tests.yaml)). The strict mypy scope is `src` and `tests`, configured in [pyproject.toml](../../pyproject.toml).
- Consult the tool-specific settings in `pyproject.toml` rather than applying blanket style rules: Ruff excludes `docs/*` and `tests/fixtures/exceptions/*`, while pytest discovers `tests`. Preserve those scope distinctions when changing fixtures or documentation.
