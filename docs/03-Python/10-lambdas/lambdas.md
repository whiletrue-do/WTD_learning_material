---
title: Lambdas
layout: default
parent: Python
has_children: false
nav_order: 10
---

# Lambdas

## Table of Contents

1. [What Are Lambdas?](#what-are-lambdas)
2. [Why Use Lambdas?](#why-use-lambdas)
3. [How to Define a Lambda](#how-to-define-a-lambda)
4. [Examples of Lambdas](#examples-of-lambdas)
5. [Common Use-Cases](#common-use-cases)
6. [Limitations and Good Practices](#limitations-and-best-practices)

## What Are Lambdas?

Lambda functions, often simply called "lambdas," are small, anonymous (unnamed) functions defined with the `lambda` keyword. Unlike standard functions declared with the `def` keyword, lambdas are used for simple operations that can be defined in a single line of code.

## Why Use Lambdas?

Lambdas are useful when you need a simple function for a short period and do not want to formally define it using `def`. They are commonly used for operations like sorting or filtering data.

## How to Define a Lambda

The general syntax for a lambda function is:

```python
lambda arguments: expression
```

- `lambda` is the keyword that declares the function.
- `arguments` are the parameters it will take.
- `expression` is the single operation it will perform.

### Examples of Lambdas

#### Basic Lambda

Here's a lambda function that adds two numbers:

```python
add = lambda x, y: x + y
print(add(5, 3))  # Output: 8
```

- `lambda x, y: x + y` is the lambda function.
- `x` and `y` are arguments.
- `x + y` is the expression that gets evaluated and returned.

#### Lambda in a List

Using a lambda to square each item in a list:

```python
numbers = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # Output: [1, 4, 9, 16]
```

## Common Use-Cases

### Sorting a List of Tuples

```python
pairs = [(1, 'one'), (4, 'four'), (3, 'three'), (2, 'two')]
pairs.sort(key=lambda pair: pair[1])
print(pairs)  # Output: [(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]
```

### Filtering a List

```python
numbers = [1, 2, 3, 4, 5]
even = list(filter(lambda x: x % 2 == 0, numbers))
print(even)  # Output: [2, 4]
```

Here are the links to the [map()](https://docs.python.org/3/library/functions.html#map) & [filter()](https://docs.python.org/3/library/functions.html#filter) built-in functions for reference.

## Limitations and Good Practices

1. Lambdas are limited to a single expression.
2. They can make code less readable if overused. As always use clear variable names to make the lambdas use clearer.
3. Ideal for short, simple tasks.

## Conclusion

Lambda functions are a powerful feature in Python for writing quick, short functions on the fly. While they have limitations, they can make your code concise for simple operations. Always consider readability and the complexity of the operation before opting for a lambda function.
