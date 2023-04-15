---
title: How to avoid "if x return x" statements using Python coding style?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the ternary operator to return x if x exists or another value otherwise return x if x else default\_value.
---

**Contents**

[TOC]

Section 1: Overview

In Python, it is common to see code with multiple `if x: return x` statements, which can make the code longer, harder to read, and harder to maintain. There are several Pythonic ways to avoid using these statements and streamline your code.

Section 2: Using Python's truthiness

In Python, many objects have boolean values that are considered "truthy" or "falsy". For example, the boolean value of an empty string, list, or dictionary is considered "falsy". You can take advantage of this feature by simply returning the object itself, without checking its truthiness.

Example:

```
def my_function(x):
    return x or None
```

In this example, if `x` is truthy, it will be returned. If `x` is falsy (e.g. an empty string), `None` will be returned.

Section 3: Using the None value

If you want to return a default value if `x` is None, you can use Python's conditional expression (also known as the ternary operator) to check if `x` is not None, and return `x` if it is, or the default value otherwise.

Example:

```
def my_function(x):
    return x if x is not None else "default value"
```

In this example, if `x` is not None, it will be returned. If `x` is None, "default value" will be returned.

Section 4: Using exception handling

If you want to raise an exception when `x` is None, you can use Python's `raise` statement to raise a `ValueError` with a custom error message.

Example:

```
def my_function(x):
    if x is None:
        raise ValueError("x cannot be None")
    return x
```

In this example, if `x` is None, a `ValueError` will be raised with the error message "x cannot be None". If `x` is not None, it will be returned. This approach is useful if you want to enforce certain conditions on the input to your function.
