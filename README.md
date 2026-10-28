# nlp-02-text-preprocessing-custom

## Project Overview

- **Author:** Alex Heyert
- **Date:** 2026 October

TODO — describe what the custom project does and which problem was chosen.

## Project Commands

TODO — replace these placeholders with the setup and run commands that have been tested, listed in the order they should be run.
```shell
# TODO — add setup command(s).
# TODO — add project run command(s).
```

## Visual Evidence

TODO — add a visual saved in the repository that provides evidence of the completed work. Use a repository-relative path, for example `docs/images/your-visual.png`.

## Developer Reference

TODO — review and modify these reference instructions and commands after customizing the code and project. Confirm every command works from a new terminal opened in the repository root before treating them as project instructions.

Follow the [Professional Python Workflow Guide](https://denisecase.github.io/pro-analytics-02/) for detailed instructions and troubleshooting.

### Initialize and Update the Python Environment

```shell
uvx pup-clean --delete
uv self update
uv python pin 3.14
uv python install
uv lock --upgrade
uv sync
uv audit
```

### Set Up and Run Git Hooks

```shell
uvx prek install --force
uvx prek update --freeze --cooldown-days 7

git add -A
uvx prek run --all-files
# Repeat if changes were made.
uvx prek run --all-files
```

### Run Common Chores

```shell
uv run ruff check . --fix
uv run ruff format .

uv run ty check
uv run python -m pytest
uv run python -m zensical build
```

### Git add-commit-push to GitHub

```shell
git add -A
git commit -m "describe your changes in quotes"
git push -u origin main
```

## Developer Tools

TODO — confirm which tools this project uses after customizing the code and project. Possible Python tools include:

- [uv](https://docs.astral.sh/uv/) — Python environments and dependencies.
- [Ruff](https://docs.astral.sh/ruff/) — Python linting and formatting.
- [ty](https://docs.astral.sh/ty/) — Python type checking.
- [pytest](https://docs.pytest.org/) — automated testing.
- [prek](https://prek.j178.dev/) — Git hooks and automated checks.
- [Zensical](https://zensical.org/) — project documentation.

## Links

- [GitHub repository](https://github.com/ajaneh/nlp-02-text-preprocessing-custom)
- Project documentation: TODO — add the documentation site link.
- Adapted example project: [NLP 02 Text Preprocessing](https://github.com/denisecase/nlp-02-text-preprocessing).
- Data source: TODO — add the source link.
