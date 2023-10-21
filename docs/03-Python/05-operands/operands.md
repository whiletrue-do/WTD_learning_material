---
title: Python Operands
layout: default
parent: Python
nav_order: 1
---

# Python Operands

## Table of Contents

1. [What are Operands?](#what-are-operands)
2. [Types of Operands](#types-of-operands)
3. [Arithmetic Operands](#arithmetic-operands)
4. [Comparison Operands](#comparison-operands)
5. [Logical Operands](#logical-operands)
6. [Identity and Membership Operands](#identity-and-membership-operands)


## What are Operands?

Operands are the values that an operator acts upon. For example, in the expression `5 + 3`, `5` and `3` are operands, and `+` is the operator. Operands are the building blocks of any expression in Python and are essential for performing operations like addition, comparison, and so on.

## Types of Operands

Operands in Python can be of various types:

- **Numbers**: Integers, floats, and complex numbers.
- **Strings**: Textual data enclosed in quotes.
- **Booleans**: `True` or `False`.
- **Lists, Tuples, Sets, Dictionaries**: Collection data types.

We will look at operands affects on strings in a separate guide.

## Arithmetic Operands

These are used with arithmetic operators to perform mathematical operations. Arithmetic operations are some of the most commonly used operands.

- Addition (`+`)
- Subtraction (`-`)
- Multiplication (`*`)
- Division (`/`)
- Floor Division (`//`)
- Modulus (`%`)
- Exponentiation (`**`)

### Arithmetic Examples

- **Addition (`+`)**: Adds two numbers.

  ```python
  result = 5 + 3  # result will be 8
  ```

- **Subtraction (`-`)**: Subtracts the right-hand operand from the left-hand operand.

    ```python
    result = 5 - 3  # result will be 2
    ```

- **Multiplication (`*`)**: Multiplies two numbers.

  ```python
  result = 5 * 3  # result will be 15
  ```

- **Division (`/`)**: Divides the left-hand operand by the right-hand operand.

  ```python
  result = 8 / 2  # result will be 4.0
  ```

- **Modulus (`%`)**: Returns the remainder of the division.

  ```python
  result = 5 % 3  # result will be 2
  ```

- **Exponentiation (`**`)**: Raises the left-hand operand to the power of the right-hand operand.

  ```python
  result = 2 ** 3  # result will be 8
  ```

- **Floor Division (`//`)**: Performs division and rounds down the result to the nearest integer.

  ```python
  result = 5 // 3  # result will be 1
  ```

## Comparison Operands

These are used with comparison operators to compare values. Comparison operators are mostly used within control flows and loops to manage a particular success or failure criteria.

- Equal to (`==`)
- Not equal to (`!=`)
- Greater than (`>`)
- Less than (`<`)
- Greater than or equal to (`>=`)
- Less than or equal to (`<=`)

### Comparison Examples

Comparison operands help you compare two values.

- **Equal (`==`)**: Checks if two values are equal.

  ```python
  result = (5 == 3)  # result will be False
  ```

- **Not Equal (`!=`)**: Checks if two values are not equal.

  ```python
  result = (5 != 3)  # result will be True
  ```

- **Greater Than (`>`)**: Checks if the left-hand operand is greater than the right-hand operand.

  ```python
  result = (5 > 3)  # result will be True
  ```

- **Less Than (`<`)**: Checks if the left-hand operand is 
less than the right-hand operand.

  ```python
  result = (5 < 3)  # result will be False
  ```

- **Greater Than or Equal (`>=`)**: Checks if the left-hand operand is greater than or equal to the right-hand operand.

  ```python
  result = (5 >= 3)  # result will be True
  ```

- **Less Than or Equal (`<=`)**: Checks if the left-hand operand is less than or equal to the right-hand operand.

  ```python
  result = (5 <= 3)  # result will be False
  ```

## Assignment Operands

Assignment operands help you assign values to variables. We have already used the `=` assignment operator i many of our previous guides

- **Assignment (`=`)**: Assigns the value from the right-hand operand to the left-hand operand.

  ```python
  x = 5  # x will be 5
  ```

The following `Add & Assign` &  operators are very helpful when working through loops and control flow operations.

## Add and Assign Operator (`+=`)

The "Add and Assign" (`+=`) operator is a convenient shorthand for updating the value of a numerical variable by adding another number to it. This operator is particularly useful when you're working with loops or when you need to increment a variable multiple times in your code.

### Long-hand Example

In the traditional way, you would add a value to a variable like this:

```python
# Initialize the variable
counter = 0

# Add 5 to the counter
counter = counter + 5  # counter will now be 5
```

In this example, we initialize a variable `counter` with the value `0`. Then, we add `5` to it using the expression `counter = counter + 5`.

### Short-hand Example

The `+=` operator simplifies this operation:

```python
# Initialize the variable
counter = 0

# Add 5 to the counter using shorthand
counter += 5  # counter will now be 5
```

Here, `counter += 5` is equivalent to `counter = counter + 5`. It's a more concise way to add `5` to the `counter`.

## Subtract and Assign Operator (`-=`)

The "Subtract and Assign" (`-=`) operator is a shorthand for reducing the value of a numerical variable by subtracting another number from it. This operator is particularly useful in loops or whenever you need to decrement a variable multiple times in your code.

### Long-hand Example

Traditionally, you would subtract a value from a variable like this:

```python
# Initialize the variable
counter = 10

# Subtract 5 from the counter
counter = counter - 5  # counter will now be 5
```

In this example, we initialize a variable `counter` with the value `10`. Then, we subtract `5` from it using the expression `counter = counter - 5`.

### Short-hand Example

The `-=` operator simplifies this operation:

```python
# Initialize the variable
counter = 10

# Subtract 5 from the counter using shorthand
counter -= 5  # counter will now be 5
```

Here, `counter -= 5` is equivalent to `counter = counter - 5`. It's a more concise way to subtract `5` from the `counter`.

### Advantages of Using `+=` & `-=`

1. **Conciseness**: The shorthand is more concise, making the code easier to read and maintain.
2. **Efficiency**: In some languages and contexts, using `-=` or `+=` can be slightly more efficient, although in Python the difference is generally negligible.
3. **Readability**: When you see `-=` or `+=`, it's immediately clear that the operation involves decrementing the value of the variable, which can make the code easier to understand at a glance.

### Other math assignment operands

the following work in the same process as the `+=` & `-=` operands explained previously and we'll only show the short hand examples.

- **Multiply and Assign (`*=`)**: Multiplies the right-hand operand by the left-hand operand and assigns the result to the left-hand operand.

  ```python
  x = 5
  x *= 3  # x will be 15
  ```

- **Divide and Assign (`/=`)**: Divides the left-hand operand by the right-hand operand and assigns the result to the left-hand operand.

  ```python
  x = 8
  x /= 2  # x will be 4.0
  ```


## Logical Operands

Logical operators are used to evaluate conditions and return a Boolean value (`True` or `False`). The primary logical operators in Python are `and`, `or`, and `not`.

- Logical AND (`and`)
- Logical OR (`or`)
- Logical NOT (`not`)

### `and` Operator

The `and` operator returns `True` if both the conditions on its sides are true.

#### Example

```python
x = 5
y = 10

result = (x > 2) and (y < 20)  # Both conditions are true, so result is True
```

### `or` Operator

The `or` operator returns `True` if at least one of the conditions on its sides is true.

#### Example

```python
x = 5
y = 30

result = (x > 2) or (y < 20)  # One condition is true, so result is True
```

### `not` Operator

The `not` operator reverses the result of the condition it precedes.

#### Example

```python
x = 5

result = not(x > 10)  # The condition (x > 10) is False, so result is True
```

## Identity and Membership Operands

Identity and membership operands are used to check for object identity and membership, respectively. These are particularly useful when you're working with complex data structures or need to compare object references.

### Identity: `is` and `is not`

The `is` operator checks if two variables point to the same object, not if they are equal. This is different from the `==` operator, which checks if the values of the variables are equal.

#### Example

```python
# Using 'is' for identity check
x = [1, 2, 3]
y = x
is_identical = (x is y)  # is_identical will be True because x and y point to the same object

# Using 'is not' for identity check
z = [1, 2, 3]
is_not_identical = (x is not z)  # is_not_identical will be True because x and z are different objects, even though their values are the same
```

- `x`, `y`, and `z` are operands.
- `is` and `is not` are the operators.
- `is_identical` and `is_not_identical` will store the boolean values `True` and `True`, respectively.

### Membership: `in` and `not in`

The `in` operator checks if a value is a member of a sequence (like a list, tuple, or string). The `not in` operator checks if a value is not a member of a sequence.

### Example

```python
# Using 'in' for membership check
my_list = [1, 2, 3, 4]
is_member = (3 in my_list)  # is_member will be True because 3 is in my_list

# Using 'not in' for membership check
is_not_member = (5 not in my_list)  # is_not_member will be True because 5 is not in my_list
```

- `my_list` is the operand.
- `in` and `not in` are the operators.
- `is_member` and `is_not_member` will store the boolean values `True` and `True`, respectively.

#### Advantages of Using Identity and Membership Operands

1. **Efficiency**: These operators provide a quick way to check for object identity and membership, which can be more efficient than using loops or other methods.
2. **Readability**: The use of `is`, `is not`, `in`, and `not in` makes the code more readable and self-explanatory.
3. **Flexibility**: These operators can be used with various data types and structures, making them versatile tools in Python programming.