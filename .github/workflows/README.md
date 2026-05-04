# GitHub Actions

## Python linter (`ruff`)

The Python linter action uses the `ruff` linter, fast and written in Rust.

### Configuration

Configuration file is `lint-python.yml`.

See documentation [here](https://docs.astral.sh/ruff)

Currently, the linter is configured to check the following issues:

- E: indentation issues, whitespace mistakes, bad comparisons such as `== NONE`
- F: Pyflakes issues such as undefined variables, unused imports and variables
- I: import sorting

Ruff's own formatter is also configured to output formatting issues.

The action is configured to run a blocking check on new/changed files and a non-blocking check on all files.

### Running

For a full local overview of the project's status, you can install `ruff` via `pip`:

```sh
pip install ruff
```

Then run:

```sh
ruff check . --output-format=github --select E,F,I
ruff format . --check
```
