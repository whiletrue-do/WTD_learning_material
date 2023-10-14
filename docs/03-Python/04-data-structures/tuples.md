---
layout: default
title: Tuples
parent: Data Structures
grand_parent: Python
nav_order: 3
---

# Tuples

## Table of Contents

1. [What are Tuples?](#what-are-tuples)
2. [When to Use Tuples](#when-to-use-tuples)
3. [Why Use Tuples](#why-use-tuples)
4. [Creating Tuples](#creating-tuples)
5. [Immutability and Its Value](#immutability-and-its-value)
6. [Tuple Unpacking](#tuple-unpacking)

---

## What are Tuples?

Tuples are another built-in Python data structure for storing an ordered collection of items. Unlike lists, tuples are immutable, meaning once you create them, you can't change them. They look like this:

```python
# A simple tuple
my_tuple = (1, 2, 3)
```

## When to Use Tuples

Tuples are your go-to when you want a list of items that should not be changed throughout the program. They're fantastic for representing things like coordinates, RGB color values, or any set of parameters that should remain constant.

## Why Use Tuples

You might be wondering, "Why would I use a tuple when a list can do the job?" Well, tuples have some advantages:

1. **Immutability**: Ensures data integrity.
2. **Hashable**: They can be used as keys in dictionaries, while lists can't.
3. **Performance**: Generally faster than lists for read-only operations.

**IMPORTANT** - Ad a Tuple is immutable you cannot change it i.e. no adding or removing!

## Creating Tuples

Creating a tuple is as simple as placing different comma-separated values between parentheses. Let's see:

```python
# An empty tuple
empty_tuple = ()

# A tuple of integers
int_tuple = (1, 2, 3)

# A tuple with mixed data types
mixed_tuple = (1, "hello", 3.4)
```

**Note on Single-Item Tuples**: If you're creating a tuple with a single item, you'll need to include a trailing comma, like so:

```python
singleton = 'hello',  # <-- note trailing comma
```

## Immutability and Its Value

Tuples are immutable, meaning you can't change them once they're created. If you try to change an item, Python will throw an error:

```python
my_tuple = (1, 2, 3)
my_tuple[0] = 4  # This will raise a TypeError
```

However, a tuple can contain mutable objects like lists:

```python
v = ([1, 2, 3], [3, 2, 1])
```

The value of immutability comes into play when you want to ensure that the data stays constant and unchangeable, which can be especially useful in multi-threaded programs.

## Tuple Unpacking

Tuples can be unpacked, meaning the values stored in a tuple can be assigned to variables. This is super handy for swapping variables or returning multiple values from a function.

```python
# Tuple unpacking
x, y, z = (1, 2, 3)
print(x)  # Output: 1
```