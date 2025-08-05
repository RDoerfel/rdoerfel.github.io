---
layout: page
title: "Simple Cookiecutter Template"
description: "A simple cookiecutter template for starting Python projects with standard structure and development tools"
category: software
date: 2025-07-11
---

When starting a new Python project, you typically need to create the same directory structure, configure `pyproject.toml`, set up development tools, and write boilerplate files. This cookiecutter template automates that process. It provides a standard project structure, configures Poetry for dependency management, and sets up common development tools like pytest, black, mypy, and flake8. It also includes an optional GitHub Actions workflow for continuous integration. It is mainly designed for lightweight data science and machine learning projects.

## What the Template Generates

The template creates a Python project with:

- Standard directory structure (source code, tests, data, docs, notebooks)
- Poetry configuration in `pyproject.toml`
- Automated test environment setup
- Linting configuration and implementation
- Development tools: pytest, black, mypy, flake8 (configurable)
- GitHub Actions workflow (optional, automatically configured)
- `.gitignore` with Python exclusions
- MIT License template

## Project Structure

Generated projects follow this layout:

```
your-project-name/
├── your_package_name/     # Main source code
├── data/                  # Data files
├── docs/                  # Documentation
├── notebooks/             # Jupyter notebooks
├── results/               # Analysis results
├── scripts/               # Utility scripts
├── tests/                 # Test files
├── .gitignore
├── LICENSE
├── README.md
└── pyproject.toml         # Poetry configuration
```

## Prerequisites and Python Version Management

Install the required tools:

```bash
pip install cookiecutter
pip install poetry
```

**Optional but recommended:**
- Install [pyenv](https://github.com/pyenv/pyenv) for Python version management
- If pyenv is available, the template can automatically configure it to use your specified Python version
- If the specified Python version is already installed, the template can set up the entire project environment automatically

## Usage

Generate a project:

```bash
cookiecutter gh:RDoerfel/simple-cookiecutter
```

The template will prompt you for:
- Project name and description
- Package name (auto-generated from project name)
- Python version
- Author information
- Which development tools to include
- Whether to set up GitHub Actions

## Configuration Options

You can choose which tools to include:

- **pytest**: Testing framework
- **coverage**: Code coverage reporting
- **black**: Code formatting
- **mypy**: Type checking
- **flake8**: Linting
- **GitHub Actions**: CI/CD pipeline

## Development Workflow

After generation, common commands are:

```bash
# Install dependencies (only if not selected during generation)
poetry install

# Run tests
poetry run pytest

# Format code
poetry run black .

# Type check
poetry run mypy package_name/

# Lint code
poetry run flake8 package_name/
```

## Tool Configurations

The template includes pre-configured settings:

**Black**: 88-character line length, target Python version matching your choice

**MyPy**: Strict type checking with warnings for untyped definitions

**Coverage**: HTML and XML reporting, excludes test files

**Pytest**: Discovers tests automatically, integrates with coverage

## GitHub Actions Integration

If enabled, the template automatically sets up a complete CI workflow that runs on push and pull requests:

1. **Automated test environment**: Configures Python and Poetry
2. **Code formatting check**: Runs black to verify formatting
3. **Linting**: Executes flake8 with configured rules
4. **Type checking**: Runs mypy for static type analysis
5. **Test execution**: Runs pytest with coverage reporting
6. **Coverage reporting**: Uploads results to codecov (if configured)

The workflow is ready to use immediately without additional configuration.

## Post-Generation Setup

The template includes a post-generation hook that automatically:
- Initializes a git repository with an initial commit
- Sets up test environment configuration
- Implements linting rules and configuration
- Configures GitHub Actions workflow (if selected)
- Offers to set up pyenv for Python version management (requires pyenv to be installed)
- Offers to install project dependencies immediately (if the specified Python version is available)

## Example Session

```bash
$ cookiecutter gh:your-username/simple-cookiecutter
project_name [My Python Project]: Data Processor
project_slug [data-processor]: 
package_name [data_processor]: 
project_short_description: Process CSV files
python_version [3.10]: 3.11
author_name [Your Name]: John Smith
use_pytest [y]: y
use_black [y]: y
# ... etc
```
