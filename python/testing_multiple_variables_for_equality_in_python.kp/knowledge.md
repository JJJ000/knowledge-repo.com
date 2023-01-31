---
title: What is the process for comparing multiple variables to one value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `==` operator to test multiple variables for equality against a single value in Python.
---

**Contents**

[TOC]

### Using Comparison Operators

The most straightforward way to test multiple variables for equality against a single value in Python is to use comparison operators. This involves using the double equals sign (==) to compare each variable to the value in question.

For example, if we wanted to test three variables (x, y, and z) against the value 5, we could use the following code:

```
if x == 5 and y == 5 and z == 5:
    print("All variables equal 5")
```

### Using the All() Function

The all() function can also be used to test multiple variables for equality against a single value. This involves passing the variables to be tested as a list to the all() function, along with the value to compare against.

For example, if we wanted to test the same three variables (x, y, and z) against the value 5, we could use the following code:

```
if all([x, y, z] == 5):
    print("All variables equal 5")
```

### Using the Any() Function

The any() function can also be used to test multiple variables for equality against a single value. This involves passing the variables to be tested as a list to the any() function, along with the value to compare against.

For example, if we wanted to test the same three variables (x, y, and z) against the value 5, we could use the following code:

```
if any([x, y, z] == 5):
    print("At least one variable equals 5")
```

### Using the All() and Any() Functions Together

The all() and any() functions can also be used together to test multiple variables for equality against a single value. This involves passing the variables to be tested as a list to the all() and any() functions, along with the value to compare against.

For example, if we wanted to test the same three variables (x, y, and z) against the value 5, we could use the following code:

```
if all([x, y, z] == 5) and any([x, y, z] == 5):
    print("All variables equal 5")
```
