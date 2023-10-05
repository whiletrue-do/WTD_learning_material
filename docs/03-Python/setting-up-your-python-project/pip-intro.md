---
layout: default
title: Python VENV
parent: Setting up your python project
grand_parent: Python intro
nav_order: 3
---

# Understanding and Using `pip` for Package Management

In this section you will understand what `pip` is, when and how to use it for package management, and how to capture and recreate your project's dependencies using a `requirements.txt` file.

## What is `pip`?

`pip` stands for "Pip Installs Packages" and is Python's package installer. It allows you to install and manage additional libraries and dependencies that are not distributed as part of the standard library.

## When to Use `pip`

You'll use `pip` when:

- **Installing New Packages**: To add new functionality to your project.
  
- **Updating Packages**: To benefit from bug fixes and new features in a package you're already using.
  
- **Removing Packages**: To uninstall packages that are no longer needed.

## Installing Packages

To install a package, open your terminal (make sure your virtual environment is activated if you're using one) and run:

```bash
pip install package_name
```

For example, to install the `requests` package, you'd run:

```bash
pip install requests
```

packages can be found at [pypi.org](https://pypi.org/)

## Removing Packages

To uninstall a package, run:

```bash
pip uninstall package_name
```

## Capturing Package State with `requirements.txt`

You can capture the current state of your project's dependencies using:

```bash
pip freeze > requirements.txt
```

This will create a `requirements.txt` file in your project directory, listing the exact versions of each package installed in your virtual environment.

## Installing Packages from `requirements.txt`

To install packages from a `requirements.txt` file, run:

```bash
pip install -r requirements.txt
```

This is particularly useful when you're setting up a new environment or sharing your project with others.

## Resources

- [Official `pip` Documentation](https://pip.pypa.io/en/stable/)
- [Real Python Guide on Python `pip`](https://realpython.com/what-is-pip/)

## Recap

You've learned what `pip` is, when and how to use it for installing, updating, and removing Python packages. You've also learned how to capture your project's dependencies in a `requirements.txt` file and how to recreate an environment from this file. Understanding `pip` and package management is crucial for any Python developer.
