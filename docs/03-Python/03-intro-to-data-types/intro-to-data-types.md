---
title: Intro to Data types
layout: default
parent: Python
nav_order: 2
---

# Understanding Basic Data Types in Python

## Objective

By the end of this section, you'll have an understanding of Python's core data types, why these types are universal across programming languages, and basic yet practical examples of their use.

We won't spend too much time on this topic, as there are numerous resources available online. Our focus here is on practical, hands-on application.

## Introduction

Data types are essential in programming; they define what kind of data can be stored and manipulated within a program. Interestingly, the core data types are consistent across most programming languages, which speaks to their fundamental role in computing.

## Core Data Types

### 1. Integer (`int`)

#### What is it?

- Represents whole numbers, both positive and negative.

#### Why is it important?

- Integers are used for operations that require counting, sorting, or anything that doesn't involve fractions.

#### Practical Example:

- Counting the number of items in a shopping cart.

  ```python
  cart_items = 5
  ```

### 2. Float (`float`)

#### What is it?

- Represents real numbers, i.e., numbers with decimal points.

#### Why is it important?

- Floats are used for calculations that require a high degree of precision.

#### Practical Example:

- Calculating a user's Body Mass Index (BMI).

  ```python
  height = 1.75  # in meters
  weight = 68.2  # in kilograms
  bmi = weight / (height ** 2)
  ```

### 3. String (`str`)

#### What is it?

- A sequence of Unicode characters.

#### Why is it important?

- Strings are used for storing and manipulating text.

#### Practical Example:

- Storing a user's first and last name.

  ```python
  first_name = "John"
  last_name = "Doe"
  ```

### 4. Boolean (`bool`)

#### What is it?

- Represents either `True` or `False`.

#### Why is it important?

- Booleans are fundamental to conditional statements and loops, enabling logical operations in programming.

#### Practical Example:

- Checking if a user is online.

  ```python
  is_online = True
  ```

## Why Are These Data Types Universal?

These core data types are universal because they are foundational to performing any kind of operation in a program, from simple calculations to complex data manipulation and logical operations.