---
title: What is the accepted way to exchange the values of two variables in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: No, there is no standardized method to swap two variables in Python.
---

**Contents**

[TOC]

# Method 1: Using a Temporary Variable

This is the most common method of swapping two variables in Python. A temporary variable is used to store the value of one of the variables, and then the values of the two variables are swapped.

```python
# Store the value of a in temp
temp = a

# Swap the values of a and b
a = b
b = temp
```

# Method 2: Using Arithmetic Operators

This method uses arithmetic operators to swap two variables without using a temporary variable.

```python
# Swap the values of a and b
a = a + b
b = a - b
a = a - b
```

# Method 3: Using XOR Operator

This method uses the XOR operator (^) to swap two variables without using a temporary variable.

```python
# Swap the values of a and b
a = a ^ b
b = a ^ b
a = a ^ b
```

# Method 4: Using Tuple Unpacking

This method uses tuple unpacking to swap two variables without using a temporary variable.

```python
# Swap the values of a and b
a, b = b, a
```
