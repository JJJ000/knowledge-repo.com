---
title: Reworded what is the difference between 'python if not ==' and 'if !='?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Both `if not ==` and `if !=` are equivalent and can be used interchangeably in Python.
---

**Contents**

[TOC]

Overview
---

In Python, both `if not ==` and `if !=` expressions are used to check whether two values are not equal to each other. While they serve the same purpose, they differ in terms of syntax and the types of values they can be applied to.

Syntax
---

The syntax for `if not ==` and `if !=` expressions is as follows:

```python
# if not ==
if value1 is not value2:
    # code block

# if !=
if value1 != value2:
    # code block
```

With `if not ==`, `is not` is used to check if two values are not equal. In contrast, `if !=` uses the `!=` operator to check if two values are not equal.

Type of Values
---

`if not ==` is more restrictive in terms of the types of values it can be applied to. Due to the use of `is not`, it can be used to check if two values are not the same object in memory. This means that it is only useful for checking if two variables point to the same object.

On the other hand, `if !=` is more general and can be used to check if two values are not equal, regardless of whether they are the same object in memory.

Example
---

Here is an example that demonstrates the difference between `if not ==` and `if !=`:

```python
# define two variables with the same value
x = [1, 2, 3]
y = [1, 2, 3]

# check if x and y are not the same object
if x is not y:
    print("x and y are not the same object")

# check if x and y are not equal
if x != y:
    print("x and y are not equal")
```

In this example, `if x is not y` will evaluate to True because `x` and `y` are two different objects in memory, even though they have the same value. Meanwhile, `if x != y` will also evaluate to True because the values of `x` and `y` are not equal, even though they are two different objects in memory.
