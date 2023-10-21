---
layout: default
title: Sets
parent: Data Structures
grand_parent: Python
nav_order: 2
---

# Sets

## Table of Contents

1. [When to Use Sets](#when-to-use-sets)
2. [Creating Sets](#creating-sets)
3. [Adding and Removing Items in Sets](#adding-and-removing-items-in-sets)
4. [Converting Lists to Sets](#converting-lists-to-sets)
5. [Set Operations](#set-operations)

---

## When to Use Sets

 So, when should you use a set? Sets are perfect for when you need an unordered collection of unique items. They're like the cool cousin of lists that don't care about order and hate duplicates. Sets are fantastic for things like:

- Membership testing: Quickly check if an item exists in a set.
- Removing duplicates: Automatically remove duplicate items.
- Mathematical operations: Perform union, intersection, and other set operations.

## Creating Sets

Creating a set is a piece of cake. You can either use curly braces `{}` or the `set()` function. But be careful! If you want an empty set, you have to use `set()`. Using empty curly braces `{}` will give you an empty dictionary instead, and we don't want that confusion.

Here's how you can create sets:

```python
# Using curly braces
fruit_set = {'apple', 'banana', 'cherry'}

# Using set() function
another_set = set(['apple', 'banana', 'cherry'])

# An empty set
empty_set = set()
```

## Adding and Removing Items in Sets

### Adding Items

You can add a single item to a set using the `add()` method, and multiple items using the `update()` method. Here's how:

```python
# Adding a single item
my_set = {1, 2, 3}
my_set.add(4)
# Output: {1, 2, 3, 4}
print(my_set)

# Adding multiple items
my_set.update([4, 5, 6])
# Output: {1, 2, 3, 4, 5, 6}
print(my_set)
```

### Removing Items

To remove items, you have a couple of options:

- `remove()`: This removes the specified item from the set. Be cautious, as it will raise a `KeyError` if the item is not found in the set.
  
- `discard()`: This also removes the specified item from the set. However, if the item is not found, it does nothing (i.e., it won't raise an error).

```python
# Using remove()
my_set = {1, 2, 3, 4, 5}
my_set.remove(5)
# Output: {1, 2, 3, 4}
print(my_set)

# Using discard()
my_set.discard(4)
# Output: {1, 2, 3}
print(my_set)

# Using discard() on a non-existent item
my_set.discard(7)  # No error
```

You can also use the `pop()` method to remove and return an arbitrary item from the set. Keep in mind that sets are unordered, so you won't know which item gets removed.

```python
# Using pop()
my_set = {1, 2, 3, 4}
item = my_set.pop()
# Output: The popped item (could be any from the set)
print(item)
```

## Converting Lists to Sets

Got a list and want to remove duplicates? You can easily convert it to a set using the `set()` function. But is this good practice? Well, it depends on your needs. If you don't care about the order of elements and just want unique items, then go for it. 

```python
# A list with duplicates
my_list = [1, 2, 2, 3, 4, 3, 5]

# Converting list to set to remove duplicates
my_set = set(my_list)

# Output: {1, 2, 3, 4, 5}
print(my_set)
```

## Set Operations

Sets in Python come with built-in methods for common set operations which can be extremely useful. Let's explore some of them:

### Union `|`

Combines all unique items from both sets.

```python
a = {1, 2, 3}
b = {3, 4, 5}
result = a | b
# Output: {1, 2, 3, 4, 5}
```

### Intersection `&`

Finds items that exist in both sets.

```python
a = {1, 2, 3}
b = {3, 4, 5}
result = a & b
# Output: {3}
```

### Difference `-`

Finds items that exist in the first set but not in the second.

```python
a = {1, 2, 3}
b = {3, 4, 5}
result = a - b
# Output: {1, 2}
```

