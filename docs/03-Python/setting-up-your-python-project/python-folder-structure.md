---
layout: default
title: python folder structure
parent: Setting up your python project
nav_order: 1
---

# The Importance of Folder Structure in Python Projects

By the end of this session, you will understand the importance of maintaining a well-organised folder structure in Python projects and how to set one up.

## Why is Folder Structure Important?

A well-organised folder structure is crucial for:

### 1. Code Maintainability

- **Easier Debugging**: A logical structure makes it easier to locate files and debug issues.
  
- **Upgradability**: A clean structure allows for easier future extensions to the codebase.

### 2. Collaboration

- **Onboarding**: A well-organised project helps new team members understand the codebase faster.
  
- **Code Reviews**: Logical organisation makes code reviews more efficient.

### 3. Reusability and Distribution

- **Modular Code**: A good structure promotes modularity, making it easier to reuse code.
  
- **Package Distribution**: A clean setup is easier to package and distribute.

## Recommended Folder Structure

Here's a commonly used folder structure for Python projects:

```
my_project/
├── src/
│   └── my_module.py
├── tests/
│   └── test_my_module.py
├── venv/
├── README.md
├── requirements.txt
└── setup.py
```

### Key Components

- **`src/`**: This is where the main codebase resides. It can be further divided into sub-folders based on functionality.

- **`tests/`**: This folder contains all test files. Keeping tests separate from the main code makes the project cleaner.

- **`venv/`**: If you're using a virtual environment, it's common to place it in a folder named `venv`.

- **`README.md`**: Always include a README to explain what your project is about, how to set it up, and how to use it.

- **`requirements.txt` or `setup.py`**: These files specify project dependencies, making it easier for others to set up your project.

## Recap

You've learned the importance of maintaining a well-organised folder structure in Python projects and how to set one up. This practice is essential for code maintainability, efficient collaboration, and easier distribution.
