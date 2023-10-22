---
title: Functions
layout: default
parent: Python
has_children: false
nav_order: 9
---

# Functions

## Table of Contents

1. [What Are Functions?](#what-are-functions)
2. [Why Use Functions?](#why-use-functions)
3. [Defining a Function](#defining-a-function)
4. [Function Arguments](#function-arguments)
5. [The Return Statement](#the-return-statement)
6. [Type Hints](#type-hints)
    - [Examples](#examples)
7. [Good Practices](#good-practices)

## What Are Functions?

Functions in Python are blocks of reusable code that perform a specific task. They can take inputs, perform actions, and return outputs.

## Why Use Functions?

Functions help to organize code, make it more readable and reusable, and allow you to perform complex tasks with fewer lines of code.

## Defining a Function

To define a function in Python, you use the `def` keyword, followed by the function name, a pair of parentheses, and a colon. The code block within the function is indented.

```python
def greet():
    print("Hello, World!")
```

## Function Arguments

Functions can take arguments to perform tasks on. Arguments are specified in the parentheses following the function name.

```python
def greet(name):
    print(f"Hello, {name}!")
```

## The Return Statement

The `return` statement is used to exit a function and return a value. If no return statement is used, the function will return `None`.

### When to Use Return

- Use `return` when you want the function to output a value that can be used later. It is important to note that the function simply provides the output and does not store it.
- Some functions may not need a `return` statement if they perform an action but don't need to send anything back.

```python
def add(x, y):
    return x + y  # returns the sum

def greet(name):
    print(f"Hello, {name}!")  # performs an action, no return needed
```

## Type Hints

As of Python 3.5+, you can add type hints to your functions to indicate the expected data types of arguments and the return value. While these hints do not enforce a data type, they make the code more readable and easier to debug.

```python
def add(x: int, y: int) -> int:
    return x + y
```

## Examples

### Basic Function

```python
def greet(name: str) -> None:
    print(f"Hello, {name}!")
```

- `def greet(name: str) -> None:` defines a function named `greet` that takes a string argument `name` and returns `None`.
- `print(f"Hello, {name}!")` is the action performed by the function.

### Function with Return

```python
def square(x: int) -> int:
    return x ** 2
```

- `return x ** 2` returns the square of `x`.

## Good Practices

1. Use descriptive function names, make sure they're clear and relevant to what the function does.
2. Keep functions small and focused on a single task, if it's between 10-30 lines (This is of course a VERY rough indicator) ask yourself "could it be broken down". Smaller functions make for easier tests... More on that later.
3. Use type hints for better readability.
4. Document your functions to explain what they do. Use comments such as `docstring` if there is some complexity or scale to your function although the aim is that your function is so simple that it doesn't need an explanation.

## Conclusion

Functions are a necessity of general programming, providing a way to modularise and reuse code. Understanding how to define functions, use arguments, and work with the `return` statement is essential for writing effective code. Type hints, introduced in Python 3.5, add an additional layer of readability and are highly recommended.
