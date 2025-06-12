# Python Template

This is Ruben's default python template.

To use it, first [install cookiecutter](https://cookiecutter.readthedocs.io/en/latest/README.html#installation). Then, run

```shell
pipx run cookiecutter gh:rbnprdy/python_template
```

To see the features of the template, check out [DEVELOPING.md](/{{%20cookiecutter.project_slug%20}}/DEVELOPING.md).

## Maintenance 

The dependency versions in [pyproject.toml](/{{%20cookiecutter.project_slug%20}}/pyproject.toml) and [.pre-commit-config.yaml](/{{%20cookiecutter.project_slug%20}}/.pre-commit-config.yaml) should be kept up-to-date. Less frequently, version updates may be needed for the actions referenced in the GitHub Actions [python.yaml](/{{%20cookiecutter.project_slug%20}}/.github/workflows/python.yaml) file.

Once it's stable, `mypy` should be replaced with [ty](https://github.com/astral-sh/ty) for what will presumably a faster and better type-checking experience.