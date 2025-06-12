# Developing

Code is linted and formatted using [ruff](https://docs.astral.sh/ruff/). Static type checking is performed using [mypy](https://mypy-lang.org). Testing is performed using [pytest](https://docs.pytest.org/en/latest).

Linting and formatting is also enforced using pre-commit, which includes some extra formatters for markdown, yaml, and toml. It also uses uv to manage dependencies.

If you use [VSCode](https://code.visualstudio.com) for development, you can install the recommended extensions:
- [python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- [mypy](https://marketplace.visualstudio.com/items?itemName=ms-python.mypy-type-checker)
- [ruff](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)

GitHub actions is used for CI, running linting, formatting, and tests on updates to main.

## Developer Installation

### uv

Package/environment management is done using [uv](https://docs.astral.sh/uv/). You can install uv globally by following [these instructions](https://docs.astral.sh/uv/getting-started/installation/).

You don't need to do anything to install the package using uv, you can just use the `uv` cli from within the project to perform any python-related actions. `uv` will automatically create and manage a virtual environment (stored under the project root in a `.env` folder).

E.g., use

```shell
uv run --dev pytest
```

to run tests,

```shell
uv python
```

to drop into a shell of the virtual environemnt's python, and

```shell
uv add DEPENDENCY_NAME
```

to install a specific dependency (or update that dependency to the latest compatible version).

### pre-commit

After cloning the repo for the first time, you should run

```shell
pre-commit install
```

to install the pre-commit hooks. If you make any changes to the pre-commit config, you should re-run against all files

```shell
pre-commit run --all-files
```

Make sure the versions of the tools in [.pre-commit-config.yaml](/.pre-commit-config.yaml) are kept up-to-date and in sync with the versions specified by `uv` in [pyproject.toml](/pyproject.toml)
