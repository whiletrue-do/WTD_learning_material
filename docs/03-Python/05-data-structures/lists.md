---
layout: default
title: Lists
parent: Data Structures
grand_parent: Python
nav_order: 1
---

# Python Lists: A Comprehensive Guide

## Table of Contents
1. [What are Lists?](#what-are-lists)
2. [Lists in Other Languages](#lists-in-other-languages)
3. [When to Use Lists](#when-to-use-lists)
4. [Creating Lists](#creating-lists)
5. [When to use a stack or queue](#when-to-use-a-stack-or-queue)
    - [Stack](#stack)
      - [Using Lists as Stacks](#using-lists-as-stacks)
    - [Queue](#queue)
      - [Using `collections.deque` as a Queue](#using-collectionsdeque-as-a-queue)
6. [List Methods](#list-methods)
7. [Accessing Lists](#accessing-lists)
8. [Slicing lists](#slicing-lists)

---

## What are Lists?

Hey there! Ready to dive into Python lists? Lists are one of Python's built-in data structures for storing an ordered collection of items. They're super flexible and can hold a mix of different data types. You can add, remove, and change items as much as you like!

```python
# A simple list
my_list = [1, 2, 3]
```

## Lists in Other Languages

If you've dabbled in other programming languages, you might know these as arrays. But Python lists are more versatile than traditional arrays in C or Java. They're dynamic, meaning they can grow or shrink in size, and they can store different types of data—pretty cool, right?

## When to Use Lists

Use lists when you have a collection of items that you want to keep in a specific order. Lists are great for keeping track of things like to-do items, the names of all your cats, or even the scores for your favorite games.

You may even choose to use Python Lists as queues or stack in your programme. Please see [when to use a stack or a queue](#when-to-use-a-stack-or-queue)

## Creating Lists

Creating a list is as simple as putting different comma-separated values between square brackets. Check this out:

```python
# An empty list
empty_list = []

# A list of integers
int_list = [1, 2, 3]

# A list with mixed data types
mixed_list = [1, "hello", 3.4]
```

**IMPORTANT NOTE ON MIXED DATA TYPES** -> Ideally please don't do it... Just because Python allows you I challenge you to find a good reason why you would want different data types in a list.

It affects readability of your code, raises the potential for errors and simply it affects type checking, why would you have a list containing booleans and strings?

## When to Use a Stack or Queue?

- **Stack**: Use a stack when you need to keep track of function calls, implement undo functionality, or manage any scenario where the last item in should be the first item out.
  
- **Queue**: Use a queue when you need to maintain a first-come, first-serve order, such as in task scheduling, breadth-first search algorithms, or any scenario where items need to be processed in the order they arrive.

Both stacks and queues are fundamental data structures and are used in a wide variety of applications, so understanding them is crucial for any programmer.

### Stack

A stack follows the Last-In-First-Out (LIFO) principle. You can think of it like a stack of books: the last book you put on the stack is the first one you'll take off.

#### Using Lists as Stacks

Python lists can be used as stacks quite easily, thanks to methods like `append()` for pushing an item onto the stack and `pop()` for popping an item off (more on methods [here](#list-methods)).

```python
# Using list as a stack
stack = []

# Push items onto the stack
stack.append("apple")
stack.append("banana")
stack.append("cherry")

print(stack)  # Output: ['apple', 'banana', 'cherry']

# Pop an item off the stack
item = stack.pop()
print(item)  # Output: 'cherry'
```

### Queue

A queue follows the First-In-First-Out (FIFO) principle. Imagine a line of people waiting for the bus: the first person in line is the first to board.

#### Using `collections.deque` as a Queue

Python's standard library offers `collections.deque`, which is designed to be fast at appending and popping from both ends and can be used as a queue.

```python
from collections import deque

# Initialize a queue
queue = deque()

# Enqueue items
queue.append("apple")
queue.append("banana")
queue.append("cherry")

print(queue)  # Output: deque(['apple', 'banana', 'cherry'])

# Dequeue an item
item = queue.popleft()
print(item)  # Output: 'apple'
```

## List Methods

Python lists come with a bunch of built-in methods to make your life easier. Let's walk through them:

### append(x)

Adds an item to the end of the list.

```python
my_list = [1, 2, 3]
my_list.append(4)
# Output: [1, 2, 3, 4]
```

### extend(iterable)

Adds multiple items to the list.

```python
my_list = [1, 2, 3]
my_list.extend([4, 5])
# Output: [1, 2, 3, 4, 5]
```

### insert(i, x)
Inserts an item at any position in the list.

```python
my_list = [1, 2, 3]
my_list.insert(1, "a")
# Output: [1, "a", 2, 3]
```

...and so on for other methods like `remove(x)`, `pop([i])`, `clear()`, `index(x[, start[, end]])`, `count(x)`, `sort(*, key=None, reverse=False)`, `reverse()`, and `copy()`.

The best place to investigate all `List` methods will be on the well be -> [Python Reference (The Right Way) - Lists](https://python-reference.readthedocs.io/en/latest/docs/list/)

## Accessing Lists

You can access list items by referring to their index number. Python lists are zero-indexed, meaning the first item is at index 0, the second at index 1, and so on.

```python
# index       0         1         2
my_list = ['apple', 'banana', 'cherry']
print(my_list[0])  # Output: 'apple'
```

You can also use negative numbers to access the list in reverse!

```python
# index      -3        -2        -1
my_list = ['apple', 'banana', 'cherry']
print(my_list[-1])  # Output: 'cherry'
```

## Slicing Lists

You can also "slice" lists, which means grabbing a subsection of the list.

to slice you utilise the colon symbol `:` between square brackets as below:

```python
# index    0  1  2  3  4  5
my_list = [0, 1, 2, 3, 4, 5]
sliced = my_list[2:5]
# Output: [2, 3, 4]
```
