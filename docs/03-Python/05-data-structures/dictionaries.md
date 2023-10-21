---
layout: default
title: Dictionaries
parent: Data Structures
grand_parent: Python
nav_order: 4
---

# Python Dictionaries: Your Go-To Guide

## Table of Contents

1. [What are Dictionaries?](#what-are-dictionaries)
2. [When to Use Dictionaries](#when-to-use-dictionaries)
3. [Creating Dictionaries](#creating-dictionaries)
4. [What Values Can Be Stored in a Dictionary?](#what-values-can-be-stored-in-a-dictionary)
5. [What Should the Key Be?](#what-should-the-key-be)
6. [Adding and Removing Items](#adding-and-removing-items)
7. [Accessing Dictionaries](#accessing-dictionaries)
8. [Dictionary Methods](#dictionary-methods)

---

## What are Dictionaries?

Dictionaries are like the Swiss Army knife of Python's data structures. They allow you to store key-value pairs, making it super easy to grab a value by its key. Unlike lists, which are indexed by numbers, dictionaries are indexed by keys, which can be any immutable type.

```python
# A simple dictionary
my_dict = {'name': 'John', 'age': 30}
```

## When to Use Dictionaries

Dictionaries are your best friend when you need a logical association between a key and a value. They're perfect for things like phone books, login credentials, and yes—even real dictionaries!

## Creating Dictionaries

Creating a dictionary is a piece of cake! You can use curly braces `{}` or the `dict()` constructor. Here's how:

```python
# Using curly braces
my_dict = {'name': 'John', 'age': 30}

# Using dict constructor
another_dict = dict(name='John', age=30)
```

**Note**: Remember, keys must be unique and immutable. So, strings, numbers, and tuples can be keys, but lists can't.

## What Should the Key Be?

In Python dictionaries, keys can be of any immutable data type. This means you can use:

- Strings
- Numbers (integers, floats)
- Tuples (only if they contain immutable types themselves, like strings, numbers, and other tuples)

However, ideally please only use Strings and integers at a push! Strings being keys makes a lot more sense and makes you code more readable.

Here's what you **can't** use as dictionary keys:

- Lists (because they are mutable)
- Dictionaries (again, mutable)
- Any other objects that are mutable

## What Values Can Be Stored in a Dictionary?

The values in a dictionary can be pretty much anything. This includes:

- Strings
- Numbers
- Lists
- Dictionaries
- Tuples
- Sets
- Custom Objects
- Even functions and methods!

In short, while keys have to be immutable, values can be both mutable and immutable.

Here are some examples to illustrate:

```python
# Using different types for keys
my_dict = {
    'name': 'John',  # string key
    42: 'answer',  # integer key
    # Again although you can use the below for keys... Ideally don't
    3.14: 'pi',  # float key
    ('tuple', 'key'): 'I am a tuple key'  # tuple key
}

# Using different types for values
another_dict = {
    'string': 'hello',
    'integer': 42,
    'float': 3.14,
    'list': [1, 2, 3],
    'dict': {'nested_key': 'nested_value'},
    'tuple': (4, 5, 6),
    'set': {7, 8, 9},
    'function': len  # yes, you can store a function!
}
```

So, when designing your dictionary, focus on using immutable types for keys and feel free to use any type for the values.

## Adding and Removing Items

Adding or updating items is straightforward. Just refer to the key and assign a value. If the key exists, its value gets updated. If it doesn't, a new key-value pair is added.

```python
# Adding an item
my_dict['email'] = 'john@email.com'

# Updating an item
my_dict['age'] = 31
```

To remove an item, you can use the `del` keyword.

```python
# Removing an item
del my_dict['age']
```

## Accessing Dictionaries

To access a value, you simply refer to its key.

```python
print(my_dict['name'])  # Output: 'John'
```

Be careful, though! If you try to access a key that doesn't exist, Python will throw a KeyError. To avoid this, you can use the `get()` method, which returns `None` if the key doesn't exist.

```python
print(my_dict.get('address'))  # Output: None
```

## Dictionary Methods

Dictionaries come with a bunch of useful methods. For example, `keys()` returns all the keys, and `values()` returns all the values.

```python
# Get all keys
print(my_dict.keys())  # Output: dict_keys(['name', 'email'])

# Get all values
print(my_dict.values())  # Output: dict_values(['John', 'john@email.com'])
```