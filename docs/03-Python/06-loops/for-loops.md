---
layout: default
title: For Loops
parent: Loops
grand_parent: Python
nav_order: 2
---

# For Loops 

## Table of Contents

- [Introduction](#introduction)
- [When to Use For Loops](#when-to-use-for-loops)
- [Basic Syntax](#basic-syntax)
- [Looping Through Sequences](#looping-through-sequences)
- [Looping Through Dictionaries](#looping-through-dictionaries)
  - [Why Two Variables?](#why-two-variables)
- [Nested For Loops](#nested-for-loops)
- [The `range()` Function](#the-range-function)
- [The `enumerate()` Function](#the-enumerate-function)
- [Using `break` and `continue`](#using-break-and-continue)
- [The `else` Clause](#the-else-clause)

## Introduction

The `for` loop in Python is a powerful tool for iterating over sequences such as lists, tuples, and strings, as well as other iterable objects like dictionaries. This guide aims to provide a comprehensive understanding of `for` loops.

## When to Use For Loops

`For` loops are ideal when you know the number of iterations in advance or when you want to traverse through a collection of items.

## Basic Syntax

The basic syntax of a `for` loop is as follows:

```python
for variable in sequence:
    # code block
```

It is important to note that the `variable` in the above code block is nothing more than a name. You will commonly see `i` or `num` as the variable. Remember you can name the `for` loop variable anything but ideally make it something applicable to the iterable items contained. Such is a `list` containing shopping items, the variable could be called `shopping_item`, etc.

## Looping Through Sequences

You can loop through lists, strings, and tuples using a `for` loop. For example:

```python
for num in [1, 2, 3]:
    print(num)
```

### Looping Through Strings

When looping through strings you will iterate through each character within that string:

```python
for char in "hello":
    print(char)
```

- for char in "hello": iterates through each character in the string "hello".
- print(char) prints each character.

## Looping Through Dictionaries

Dictionaries in Python are collections of key-value pairs. To loop through dictionaries, you can use methods like `.items()`, `.keys()`, and `.values()`.

### Using `.items()`

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
for key, value in my_dict.items():
    print(f"Key: {key}, Value: {value}")
```

#### Why Two Variables?

When you use `.items()`, it returns a tuple containing the key and value for each item in the dictionary. Therefore, you need two variables (`key` and `value` in this case) to unpack this tuple into its individual components. This is why we use `for key, value in my_dict.items():`.

### Using `.keys()`

You can simply loop through keys:

```python
for key in my_dict.keys():
    print(f"Key: {key}")
```

### Using `.values()`

You can also simply loop through the values:

```python
for value in my_dict.values():
    print(f"Value: {value}")
```

## Nested Loops in Python

### Why Nested Loops Are Used

Nested loops are loops within loops. They are useful for iterating through multi-dimensional data structures like lists of lists, matrices, or nested dictionaries. They can also be used for tasks that require multiple passes over the data, such as sorting algorithms or searching algorithms.

### Example: Finding an Element in a List of Lists

Here's an example where we use a nested `for` loop to find an element in a list of lists:

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

target = 5
found = False

for row in matrix:
    for element in row:
        if element == target:
            print(f"Target {target} found!")
            found = True
            break
    if found:
        break
```

#### Explanation

- `matrix` is a list of lists, representing a 3x3 matrix.
- `target` is the element we want to find.
- The outer loop iterates through each row in the matrix.
- The inner loop iterates through each element in the row.
- If the target element is found, both loops are terminated using `break`.

#### Potential Pitfalls

1. **Complexity**: Nested loops increase the computational complexity, often making it O(n^2) or worse. This can lead to performance issues for large datasets.
  
2. **Readability**: Nested loops can make the code harder to read and maintain. Always comment your code and consider breaking out nested loops into separate functions if possible.

3. **Infinite Loops**: Be cautious when using `while` loops as nested loops. Ensure that the condition for the `while` loop will eventually become `False`; otherwise, you'll end up with an infinite loop.

4. **Debugging**: Errors can be harder to debug in nested loops, especially if multiple variables are being changed in the loops.

5. **Early Exit**: If you're using `break` to exit a nested loop, it will only exit the innermost loop. If you need to exit all loops, you'll have to use a flag variable or some other mechanism, as shown in the example.

By being aware of these pitfalls, you can write nested loops that are both efficient and maintainable.

## Example: Iterating Through a Nested Dictionary

Suppose you have a nested dictionary that represents a collection of books, categorized by genre. Each genre contains a dictionary of books and their authors.

```python
books_by_genre = {
    'Science Fiction': {
        'Dune': 'Frank Herbert',
        'Neuromancer': 'William Gibson',
        'Foundation': 'Isaac Asimov'
    },
    'Fantasy': {
        'The Hobbit': 'J.R.R. Tolkien',
        'Harry Potter': 'J.K. Rowling',
        'A Song of Ice and Fire': 'George R.R. Martin'
    },
    'Mystery': {
        'The Da Vinci Code': 'Dan Brown',
        'Murder on the Orient Express': 'Agatha Christie',
        'Gone Girl': 'Gillian Flynn'
    }
}
```

To iterate through this nested dictionary and print out each genre, book, and author, you can use nested `for` loops:

```python
for genre, books in books_by_genre.items():
    print(f"Genre: {genre}")
    for book, author in books.items():
        print(f"  Book: {book}, Author: {author}")
```

### Explanation

- The outer loop iterates through each genre and its corresponding books dictionary in `books_by_genre`.
  - `genre` holds the genre name (e.g., 'Science Fiction').
  - `books` holds the dictionary of books in that genre.

- The inner loop iterates through each book and its corresponding author in the `books` dictionary.
  - `book` holds the book name (e.g., 'Dune').
  - `author` holds the author of the book (e.g., 'Frank Herbert').

This way, you can access each level of the nested dictionary. The outer loop gives you access to the genres, and the inner loop gives you access to the books and authors within each genre.

## The `range()` Function

The `range()` function generates a sequence of numbers, useful for looping a specific number of times.

```python
for i in range(5):
    print(i)
```

## The `enumerate()` Function

`enumerate()` adds a counter to an iterable, allowing you to track the index of each item. As you can see in the below example it provides two variables much like we discussed in looping through dictionaries using the `.items()` method.

```python
for index, value in enumerate(['a', 'b', 'c']):
    print(f"Index: {index}, Value: {value}")
```

## Using `break` and `continue`

- `break`: Exits the loop when a certain condition is met.
- `continue`: Skips the current iteration and proceeds to the next one.

## The `else` Clause

The `else` clause executes after the `for` loop completes, but only if the loop was not terminated by a `break` statement.

```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```
