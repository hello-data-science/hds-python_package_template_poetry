![Work in Progress](https://img.shields.io/badge/Status-WIP-yellow)
![Template](https://img.shields.io/badge/Template-blue)
![Python](https://img.shields.io/badge/Python-3.8%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue)
![Poetry](https://img.shields.io/badge/Poetry-Package%20Manager-blue)

# Python Package Template

A template repository for developing Python packages using Poetry in a VSCode devcontainer. Comes pre-configured with Poetry and Quarto for package documentation.

## Features

- Devcontainer configuration for VSCode
- Poetry for dependency management
- Quarto for documentation
- Pre-configured development environment

## Quick Start

1. Click "Use this template" to create a new repository
2. Clone your new repository
3. Open in VSCode with devcontainer extension
4. VSCode will prompt to reopen in container - accept this

## Project Setup

1. Initialize Poetry project:
```bash
poetry init
```

2. Set up development dependencies:
```bash
poetry add --group dev pytest
poetry add --group dev quartodocs
```

3. Create your package structure:
```bash
mkdir your_package_name
touch your_package_name/__init__.py
```

## Documentation

Documentation is handled through Quarto. To build the documentation:

```bash
quarto render
```

## Example Project

After creating a new repository from this template:

1. Clone your repository and open in VSCode
   ```bash
   git clone <your-repo-url>
   code <repo-directory>
   ```

2. When prompted, reopen in container (or use Command Palette: "Reopen in Container")

3. Initialize your Poetry project (update with your details)
   ```bash
   poetry init --name your-package-name \
               --description "Your package description" \
               --author "Your Name <your.email@example.com>" \
               --python "^3.8" \
               --dependency python="^3.8" \
               --dev-dependency pytest="^7.0" \
               --dev-dependency quartodocs="^0.1.0" \
               -n
   ```

4. Create initial package structure
   ```bash
   touch __init__.py
   ```

5. Add core dependencies for development
   ```bash
   poetry add --group dev pytest pytest-cov black isort mypy pylint pre-commit
   ```

6. Create basic test structure
   ```bash
   mkdir tests
   touch tests/__init__.py
   touch tests/test_basic.py
   ```

7. Initialize git pre-commit hooks
   ```bash
   pre-commit install
   ```

8. Start developing your package!

Your project is now set up with:
- Poetry for dependency management
- pytest for testing
- Code quality tools (black, isort, mypy, pylint)
- pre-commit hooks for consistent code quality
- Quarto for documentation