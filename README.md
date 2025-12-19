# Python Starter Template

This is a template for creating Python projects using the [Copier](https://copier.readthedocs.io/) library. Copier is a tool that allows copying and customizing project templates efficiently. The generated projects are optimized for use with [uv](https://github.com/astral-sh/uv), a fast Python package installer and resolver.

## Features

- Basic Python project structure with `src/` layout.
- `pyproject.toml` file for project configuration, compatible with uv and modern Python packaging.
- Basic CLI implemented with Click.
- Tests with pytest.
- Pre-commit hooks configuration.
- CI/CD workflow with GitHub Actions.
- MIT License.

## Requirements

- Python 3.10+
- [uv](https://github.com/astral-sh/uv) (includes uvx for running tools without global installation)

## Installing uv

uv is recommended for managing dependencies and running tools in the generated projects.

```bash
# On macOS and Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# On Windows
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.sh | iex"
```

## Usage

To create a new Python project based on this template:

### Option 1: Using a local copy

1. Install uv as described above.
2. Clone or download this repository.
3. Run the following command in the template's root directory:

```bash
uvx copier copy . /path/to/new/project
```

### Option 2: Directly from Git repository

If the template is hosted on a Git repository (e.g., GitHub), you can copy it directly without cloning:

```bash
uvx copier copy https://github.com/alexmarco/python-starter /path/to/new/project
```

uvx allows running Copier without installing it globally.

4. Copier will prompt you to provide values for the template variables, such as:
   - `project_name`: The project name.
   - `package_name`: The Python package name.
   - Other values defined in `copier.yml`.

5. Once completed, you will have a new Python project ready to use.

## Generated Project Structure

```
new_project/
├── src/
│   └── package_name/
│       ├── __init__.py
│       ├── __main__.py
│       └── cli.py
├── tests/
│   └── test_example.py
├── .github/
│   └── workflows/
│       └── ci.yml
├── .pre-commit-config.yaml
├── pyproject.toml
├── README.md
└── LICENSE
```

## Development

After generating the project, you can manage dependencies and run commands using uv (recommended) or pip.

### With uv (recommended):

- Install dependencies: `uv pip install -e .`
- Run tests: `uv run pytest`
- Run the CLI: `uv run python -m package_name`
- Set up pre-commit: `uv run pre-commit install`

### With pip (alternative):

- Install dependencies: `pip install -e .`
- Run tests: `pytest`
- Run the CLI: `python -m package_name`
- Set up pre-commit: `pre-commit install`

## Contributing

If you want to contribute to this template, please open an issue or send a pull request.

## License

This project is under the MIT License. See [LICENSE](LICENSE) for more details.