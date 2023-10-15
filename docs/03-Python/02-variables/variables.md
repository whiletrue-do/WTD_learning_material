---
title: Python variables
layout: default
parent: Python
nav_order: 2
---

# Understanding Variables in Python

## Objective

By the end of this section, you'll understand what variables are, why they are used, how to name them according to PEP 8 guidelines, and some unique characteristics of Python variables.

## Introduction

Variables are one of the foundational elements in any programming language. They are used to store data that can be used and manipulated throughout a program. Let's dive into the world of variables in Python.

## What is a Variable?

A variable is essentially a name that represents some value stored in the computer's memory. Think of it as a labeled box where you can put stuff you might need later.

## Why Use Variables?

Variables are used for several reasons:

- **Data Storage**: To keep data for use at a later time.
- **Reusability**: To use the same data in multiple places.
- **Readability**: To make the code more understandable.

## Naming Variables

### PEP 8 Guidelines

Python has a style guide known as PEP 8, which provides naming conventions for variables:

- Use lowercase with underscores for variable names (`my_variable`).
- Avoid using reserved words (`True`, `False`, `None`, etc.).
- Make the name descriptive and not too long.

### Interpreter Acceptance

Python's interpreter does have some rules:

- Variable names must start with a letter or an underscore.
- The rest of the name can contain letters, numbers, and underscores.
- Names are case-sensitive.


## Variables as References to Data

In Python, variables don't "contain" data; they "refer to" or "point to" data. This is an important distinction that affects how variables behave when you manipulate them. 

### Reassigning Variables

Because variables are references to data, they can be easily reassigned to point to different data types or different values altogether.

```python
# `x` is pointing to an integer object
x = 42

# Now `x` is pointing to a string object
x = "hello"

# And now it's pointing to a list
x = [1, 2, 3]
```

In the example above, the variable `x` initially points to an integer object (`42`). Later, it's reassigned to point to a string object (`"hello"`), and then to a list (`[1, 2, 3]`). At each step, the variable `x` changes what it's pointing to, but it remains a variable.

### Implications

Understanding that variables are references has several implications:

- **Mutable Objects**: If a variable points to a mutable object like a list, changes to the object are reflected in every variable that points to it.
  
- **Immutable Objects**: For immutable objects like strings and tuples, variables can be reassigned, but the objects they point to can't be changed.

- **Variable Reassignment**: A variable can be reassigned to point to any type of object, irrespective of its original type.

## Python's Unique Characteristics

### No Explicit Public/Private Variables

In many programming languages, you'll find explicit keywords like `public` and `private` to define the accessibility of a variable. Python doesn't have these explicit modifiers. However, it does have some conventions to indicate the intended level of variable privacy.

#### Public Variables

By default, all variables are public. This means they can be accessed and modified from anywhere in your code.

```python
# This is a public variable
my_public_variable = "I can be accessed from anywhere!"
```

#### "Protected" Variables

If a variable name is prefixed with an underscore (`_`), it's treated as "protected" by convention. This means that the variable is intended for internal use within the class/module, and it's considered polite to not access it directly from outside.

```python
# This is a protected variable
_my_protected_variable = "I'm intended for internal use."
```

While the Python interpreter won't stop you from accessing or modifying `_my_protected_variable` directly, doing so is generally frowned upon.

#### "Private" Variables by Convention

Although Python doesn't have explicit private variables, names with double underscores before the name (and none or just one after) are "name-mangled" to include the name of the containing class. This makes it harder (but not impossible) to access them unintentionally.

```python
# This is as close as you get to a private variable in Python
__my_almost_private_variable = "I'm harder to access unintentionally."
```

In practice, this is rarely used, and the single underscore convention for protected variables is generally preferred.

### No Built-in Constants

Python doesn't have built-in support for constants. However, by convention, fully capitalised variable names are used to indicate a variable should be treated as a constant, like `PI = 3.14159`.

## Potential Pitfalls

- **Overwriting**: Since Python doesn't have explicit public/private variables, it's easy to accidentally overwrite variable values.
  
- **Immutability**: Some data types like tuples and strings are immutable, meaning their content can't be changed once created.

## Recap

You've learned what variables are, why they're important, how to name them, and some unique aspects of Python variables. Understanding variables is crucial for effective Python programming, especially given some of the language's unique characteristics.
