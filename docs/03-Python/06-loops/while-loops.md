---
layout: default
title: While Loops
parent: Loops
grand_parent: Python
nav_order: 1
---

# While Loops

## Table of Contents

- [Introduction to While Loops](#introduction-to-while-loops)
- [When to Use While Loops](#when-to-use-while-loops)
- [Using While Loops with Lists and Dictionaries](#using-while-loops-with-lists-and-dictionaries)
- [Common Pitfalls with While Loops](#common-pitfalls-with-while-loops)
- [Using `break` and `continue`](#using-break-and-continue)

## Introduction to While Loops

A `while` loop is a control flow statement that allows you to execute a block of code repeatedly as long as a condition is met. The loop will continue to execute until the condition specified evaluates to `False`.

```python
while condition:
    # code to be executed
```

## When to Use While Loops

Use `while` loops when:

- You don't know the number of iterations in advance.
- You want to maintain a state until a certain condition is met.

## Using While Loops with Lists and Dictionaries

### With Lists

```python
# Removing all instances of a value from a list
numbers = [1, 2, 3, 4, 5, 3, 6]
while 3 in numbers:
    numbers.remove(3)
```

- `numbers` is a list containing integers.
- `while 3 in numbers:` checks if the value `3` is in the list.
- `numbers.remove(3)` removes the first occurrence of `3` in the list.

### With Dictionaries

```python
# Removing all key-value pairs with value 'None'
my_dict = {'a': 1, 'b': None, 'c': 2, 'd': None}
while None in my_dict.values():
    for key, value in list(my_dict.items()):
        if value is None:
            del my_dict[key]
```

- `my_dict` is a dictionary containing key-value pairs.
- `while None in my_dict.values():` checks if any value in the dictionary is `None`.
- `for key, value in list(my_dict.items()):` iterates through a list of key-value pairs.
- `if value is None:` checks if the value is `None`.
- `del my_dict[key]` deletes the key-value pair where the value is `None`.

## Common Pitfalls with While Loops

1. **Infinite Loops**: Make sure the loop condition will eventually become `False`; otherwise, the loop will run indefinitely.
2. **High CPU Usage**: A `while` loop with a trivial condition can consume a lot of CPU.
3. **Logic Errors**: Ensure that the loop condition and the loop body are in sync to avoid unexpected behavior.

## Using `break` and `continue`

### Using `break`

The `break` statement allows you to exit a `while` loop prematurely when a certain condition is met.

```python
count = 0
while True:
    print(count)
    count += 1
    if count >= 5:
        break
```

- `while True:` creates an infinite loop.
- `print(count)` prints the current value of `count`.
- `count += 1` increments `count` by 1.
- `if count >= 5:` checks if `count` is greater than or equal to 5.
- `break` exits the loop.

### Using `continue`

The `continue` statement allows you to skip the rest of the loop body and continue with the next iteration.

```python
count = 0
while count < 5:
    count += 1
    if count == 3:
        continue
    print(count)
```

- `while count < 5:` checks if `count` is less than 5.
- `count += 1` increments `count` by 1.
- `if count == 3:` checks if `count` is equal to 3.
- `continue` skips the rest of the loop body for the current iteration.
- `print(count)` prints the current value of `count`.
