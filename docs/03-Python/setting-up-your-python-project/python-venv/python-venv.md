---
layout: default
title: Python VENV
parent: Setting up your python project
grandparent: Python Intro
nav_order: 1
---

# Understanding and Using Python's `venv` Module

## Objective

In this section you will understand why and how to use Python's built-in `venv` module to manage isolated Python environments.

## Why Use `venv`?

Python's `venv` module comes pre-installed with Python (starting from Python 3.3), so you don't need to install anything extra. Using `venv` allows you to:

- **Isolate Dependencies**: Each project can have its own dependencies, irrespective of what dependencies every other project has.
  
- **Prevent Conflicts**: Using a virtual environment prevents package and version conflicts at the global level, ensuring that your project's dependencies don't interfere with each other.

- **Reproducibility**: Makes it easier to share the project and its dependencies.

## Creating a Virtual Environment

To create a virtual environment, navigate to your project directory in the terminal and run:

```bash
python -m venv venv
```

or

```bash
python -m venv .venv
```

**Note**:

- Naming it `venv` or `.venv` is a common convention.
- The dot notation (`.venv`) is used to indicate hidden files on macOS and Linux. On Windows, the file won't be hidden but the naming convention is still widely accepted.

## Activating the Virtual Environment

### macOS and Linux

To activate the virtual environment, run:

```bash
source venv/bin/activate
```

or if you named it `.venv`:

```bash
source .venv/bin/activate
```

### Windows

To activate the virtual environment, run (please note it's best to be using git Bash):

```cmd
.\venv\Scripts\Activate
```

or if you named it `.venv`:

```cmd
.\.venv\Scripts\Activate
```

## Deactivating the Virtual Environment

To deactivate the virtual environment and return to the global Python environment, simply run:

```bash
deactivate
```

## Additional Tips

- Always add `venv` or `.venv` to your `.gitignore` file if you're using Git to prevent the virtual environment from being committed to version control.

- You can use the `pip freeze > requirements.txt` command within an activated virtual environment to save your project's dependencies in a `requirements.txt` file. This makes it easier to recreate the environment later.

## Resources

- [Python Official `venv` Documentation](https://docs.python.org/3/library/venv.html)
- [Real Python Guide on Python Virtual Environments](https://realpython.com/python-virtual-environments-a-primer/)

## Recap

You've learned why it's crucial to use Python's built-in `venv` module for dependency management and how to create, activate, and deactivate virtual environments on macOS and Windows. This practice is essential for effective Python project management and collaboration.
