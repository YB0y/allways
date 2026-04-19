# Contributing to Allways

## Development Setup

1. Clone the repository and install dependencies:

   ```bash
   uv sync --group dev
   ```

2. Install git hooks:

   ```bash
   uv run pre-commit install --install-hooks
   ```

   This installs pre-commit and pre-push hooks. Ruff lint/format runs on every
   commit; pytest runs before push.

3. Run all checks manually:

   ```bash
   uv run pre-commit run --all-files                        # pre-commit hooks
   uv run pre-commit run --all-files --hook-stage pre-push  # pre-push hooks
   ```

4. To skip hooks for WIP commits or pushes:

   ```bash
   git commit --no-verify -m "WIP: ..."
   git push --no-verify
   ```

## Code Style

- Line length: 120 characters
- Single quotes for strings
- Ruff linting with E, F, I rules

## Pull Requests

1. Create a feature branch
2. Make your changes
3. Ensure tests pass
4. Submit a pull request
