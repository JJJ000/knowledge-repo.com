---
title: Can you explain the distinction between nan and none?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: None represents the absence of a value, while NaN represents a value that is undefined or unrepresentable.
---

**Contents**

[TOC]

## NaN

`NaN` stands for "Not a Number" and is a special value of the `float` data type in Python. It is typically used to represent the result of a mathematical operation that is undefined or cannot be computed, such as `0.0 / 0.0`. 

- `NaN` is a floating-point value. 
- It represents undefined and non-representable values, such as division by zero. 
- `NaN` is a sign that there is some problem in the computation, such as arithmetic overflow or underflow or a domain error. 
- `NaN` has the property that it is not equal to any value, even itself `NaN != NaN` evaluates to `True`. 


## None

`None` is a built-in constant in Python that represents the absence or lack of a value. It is often used as a default return value for a function that doesn't return anything, or to indicate that a variable or argument doesn't have a meaningful value.

- `None` is a value that represents the absence of a value.
- It is used as a default value for arguments of functions or other variables. 
- `None` is conceptually different from `False` and `0`. 
- `None` evaluates to False in a boolean context. 
- `None` is not the same as an empty string or an empty list, which are both non-None objects.


## Differences between NaN and None

1. Type

`NaN` is a floating-point value, while `None` is a built-in constant.

2. Meaning

`NaN` represents undefined and non-representable values, such as division by zero. `None` represents the absence or lack of a value.

3. Equality

`NaN` is not equal to any value, including itself. `None` is equal only to itself.

4. Operations

`NaN` can be used in mathematical operations, but may cause problems if not handled properly. `None` cannot be used in mathematical operations.

In summary, `NaN` and `None` may seem similar, but they have different meanings and are used in different contexts. It is important to understand the differences to avoid confusion and errors in Python code.
