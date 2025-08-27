![Work in Progress](https://img.shields.io/badge/Status-WIP-yellow)
![Template](https://img.shields.io/badge/Template-blue)
![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.11-blue)
![Poetry](https://img.shields.io/badge/Poetry-Package%20Manager-blue)

# Python Package Template

A template repository for developing Python packages using Poetry in a VSCode devcontainer. Comes pre-configured with Poetry and Quarto for package documentation.

## Features

- Devcontainer configuration for VSCode
- Poetry for dependency management
- Quarto for documentation
- Pre-configured development environment

## Quick Start

**Pre-requisites:** Ensure you have the following installed on your system: [Visual Studio Code (VSCode)](https://code.visualstudio.com/) and [Docker Desktop](https://www.docker.com/products/docker-desktop)

1. Click "Use this template" to create a new repository
2. Clone your new repository
3. Open in VSCode with devcontainer extension
4. VSCode will prompt to reopen in container - accept this (will take a few minutes)

> Alternatively, click 'Use this template' in this repository, then select 'Open in a codespace' to try it out directly in your browser.

## Project Setup

Open a terminal in your container workspace and run the following:

1. Initialize Poetry project:
```bash
poetry init
```

2. Set up development dependencies:
```bash
poetry add --group dev pytest
poetry add --group dev quartodoc
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

> Alternatively, replace steps 1 and 2 by clicking 'Use this template' in this repository, then select 'Open in a codespace' to try it out directly in your browser.

1. Clone your repository and open in VSCode
   ```bash
   git clone <your-repo-url>
   code <repo-directory>
   ```

2. When prompted, reopen in container (or use Command Palette: "Reopen in Container")

3. Initialize your Poetry project (update with your details)
   ```bash
   poetry init --name hellopy \
            --description "Your package description" \
            --author "Your Name <your.email@example.com>" \
            --python "^3.11" \
            -n
   ```

4. Create initial package structure
   ```bash
   mkdir hellopy && \
   touch hellopy/__init__.py && \
   touch hellopy/hello.py
   ```

5. Populate `hello.py` with the following
   ```python
    def hello():
        """
        Print a greeting message.

        Example usage:
        ```{python}
        from hellopy.hello import hello
        hello()
        ```
        """
        print("Hello!")
   ```

6. Install your package in editor mode, add IPython and Jupyter to aid development, and activate virtual 
    ```bash
    poetry install && \
    poetry add --group dev ipython jupyter
    ```

7. Activate virtual environment
   ```bash
   source .venv/bin/activate
   ```

8. Start Ipython (or an interactive Jupyter window)
   ```bash
   ipython
   ```

9.  In Ipython, import `hello()`
    ```python
    from hellopy.hello import hello
    ```

10. Enjoy developing your package!
    ```python
    # Try editing `hello.py` and re-running the `hello()` command
    hello()
    ```