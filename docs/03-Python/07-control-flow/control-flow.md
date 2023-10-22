---
title: Control Flow
layout: default
parent: Python
has_children: false
nav_order: 7
---

# Control Flow

Control flow is a fundamental concept in programming that allows you to execute different blocks of code based on certain conditions. Python provides several control flow statements including `if`, `elif`, and `else`, as well as loops like `for` and `while`. In this guide, we'll explore how to use these statements effectively, particularly within loops for lists and dictionaries.

## Table of Contents

1. [The `if` Statement](#the-if-statement)
2. [The `elif` and `else` Statements](#the-elif-and-else-statements)
3. [Using Control Flow in Loops](#using-control-flow-in-loops)
    - [With Lists](#with-lists)
    - [With Dictionaries](#with-dictionaries)
4. [Combining Control Flow with Logical Operators](#combining-control-flow-with-logical-operators)


## The `if` Statement

### Structure

The `if` statement evaluates a condition and executes the subsequent indented block of code if the condition is `True`.

```python
if condition:
    # code to execute if condition is True
```

### Example

```python
x = 10
if x > 5:
    print("x is greater than 5")
```

## The `elif` and `else` Statements

### Structure

The `elif` (else if) and `else` statements are used for multiple conditions. They follow an `if` or another `elif` statement.

```python
if condition1:
    # code to execute if condition1 is True
elif condition2:
    # code to execute if condition2 is True
else:
    # code to execute if none of the above conditions are True
```

### Example

```python
x = 10
if x > 20:
    print("x is greater than 20")
elif x > 5:
    print("x is greater than 5 but not greater than 20")
else:
    print("x is 5 or less")
```

## Using Control Flow in Loops

### With Lists

You can use control flow statements within loops to perform different actions for different elements in a list.

#### Example

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    if number % 2 == 0:
        print(f"{number} is even")
    else:
        print(f"{number} is odd")
```

### With Dictionaries

Similarly, you can use control flow within loops for dictionaries to perform actions based on key-value pairs.

#### Example

```python
student_grades = {'Alice': 'A', 'Bob': 'B', 'Charlie': 'C'}
for name, grade in student_grades.items():
    if grade == 'A':
        print(f"{name} is an excellent student")
    elif grade == 'B':
        print(f"{name} is a good student")
    else:
        print(f"{name} needs improvement")
```

Certainly! Let's add a section that explains how control flow statements can be combined with logical operators like `and`, `or`, and `not` for more complex conditions.

## Combining Control Flow with Logical Operators

Logical operators such as `and`, `or`, and `not` can be used to create more complex conditions in your control flow statements.

### Structure

Here's how you can combine them:

```python
if condition1 and condition2:
    # code to execute if both conditions are True

if condition1 or condition2:
    # code to execute if at least one condition is True

if not condition1:
    # code to execute if condition1 is False
```

### Examples

#### Using `and` in a List Loop

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    if number > 2 and number < 5:
        print(f"{number} is greater than 2 and less than 5")
```

#### Using `or` in a Dictionary Loop

```python
student_grades = {'Alice': 'A', 'Bob': 'B', 'Charlie': 'C'}
for name, grade in student_grades.items():
    if grade == 'A' or grade == 'B':
        print(f"{name} is doing well")
```

#### Using `not` in a List Loop

```python
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    if not number % 2 == 0:
        print(f"{number} is not even")
```

By combining control flow statements with logical operators, you can create more nuanced conditions and make your code more flexible and powerful. Although, always remember the importance of **readability**!