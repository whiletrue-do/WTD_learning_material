---
title: Loops
layout: default
parent: Python
has_children: true
nav_order: 6
---


# Introduction to Looping in Python

## Table of Contents
1. [What is Looping?](#what-is-looping)
2. [Why Do We Use Looping?](#why-do-we-use-looping)
3. [Types of Loops](#types-of-loops)
    - [While Loop](#while-loop)
    - [For Loop](#for-loop)
4. [Iterable Data Structures](#iterable-data-structures)

---

## What is Looping?

Ever found yourself needing to repeat the same action multiple times in your code? That's where loops come in. Looping is a fundamental concept in programming that allows you to execute a block of code repeatedly. 

In Python, you primarily have two types of loops to accomplish this: `while` loops and `for` loops.

## Why Do We Use Looping?

Imagine having to print numbers from 1 to 100 manually, or what if you had to process each item in a list one by one? Sounds tedious, right? Loops automate repetitive tasks and make your code more efficient, readable, and manageable.

## Types of Loops

### While Loop

The `while` loop continues execution as long as a specified condition evaluates to `True`. It's like a repeating `if` statement.

```python
# While loop example
count = 0
while count < 5:
    print(f"Count is {count}")
    count += 1
```

### For Loop

The `for` loop is used for iterating over a sequence (list, tuple, dictionary, set, or string). It's like saying, "For each item in this list, do this."

```python
# For loop example
for i in range(5):
    print(f"Count is {i}")
```

## Iterable Data Structures

In Python, several data structures are `"iterable"` meaning you can loop through them. Here's a quick list:

- **Lists**: Loop through each element.
- **Tuples**: Similar to lists, but immutable.
- **Dictionaries**: Loop through keys, values, or key-value pairs.
- **Sets**: Loop through unique elements.
- **Strings**: Loop through each character.

```python
# Looping through a list
for item in [1, 2, 3, 4]:
    print(item)

# Looping through a dictionary
for key, value in {'a': 1, 'b': 2}.items():
    print(f"Key: {key}, Value: {value}")
```
