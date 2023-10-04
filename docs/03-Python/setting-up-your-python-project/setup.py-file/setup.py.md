---
layout: default
title: The setup.py file
parent: Setting up your python project
grand_parent: Python intro
nav_order: 4
---


# Understanding and Using the `setup.py` File

By the end of this section you will understand what the `setup.py` file is, how to set it up, and why using `find_packages()` is important when creating packages in your project.

## What is `setup.py`?

The `setup.py` file is a build script for `setuptools`. It tells `setuptools` about your package (such as the name and version) as well as files to include. This file is what enables you to package and distribute your Python project, allowing others to easily install it.

## How is it Set Up?

A basic `setup.py` file looks something like this:

```python
from setuptools import setup, find_packages

setup(
    name='my_package',
    version='0.1',
    packages=find_packages(),
    install_requires=[
        'required_package1',
        'required_package2',
    ],
)
```

Here's what each argument means:

- `name`: The name of your package.
- `version`: The package version.
- `packages`: The Python packages to include. This is usually specified using `find_packages()`.
- `install_requires`: A list of dependencies that will be installed with your package.

## Importance of `find_packages()`

The `find_packages()` function is used to discover and include all Python packages in your project. This is important because:

- **Automatic Discovery**: You don't have to manually list each package or sub-package.
  
- **Ease of Use**: It makes your package easily reusable. Users can simply install your package and import any packages or modules contained within it.

- **Project Scalability**: As your project grows, `find_packages()` will automatically discover new packages or sub-packages, making it easier to manage.

## Additional Tips

- If your project includes non-Python files (like data files), you can include them using the `package_data` argument in `setup()`.

- You can specify additional metadata like `author`, `author_email`, `description`, etc., to make your package more informative.

## Resources

- [Official Python Packaging Authority `setup.py` Guide](https://packaging.python.org/guides/distributing-packages-using-setuptools/#setup-py)
- [Real Python Guide on Python Packages](https://realpython.com/tutorials/packages/)

## Recap

You've learned what the `setup.py` file is, how to set it up, and why using `find_packages()` is crucial when creating packages in your project. Understanding how to properly configure `setup.py` is essential for anyone looking to distribute their Python project.
```

Feel free to add or remove sections as you see fit!