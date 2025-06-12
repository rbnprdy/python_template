# {{ cookiecutter.project_name }}

[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![Checked with mypy](https://www.mypy-lang.org/static/mypy_badge.svg)](https://mypy-lang.org/)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

{{ cookiecutter.project_short_description }}

## Installation Instructions

> [!Important]
> If you are developing `{{ cookiecutter.project_slug }}`, you should use the installation instructions from [DEVELOPING.md](/DEVELOPING.md) instead.

To install this repo, just clone it and install using pip:

```shell
cd {{ cookiecutter.project_slug }}
pip install -r requirements.txt
pip install .
```