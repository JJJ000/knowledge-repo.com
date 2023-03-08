---
title: Can you explain the meaning of "1..__truediv__" in Python and confirm whether Python supports a "dot dot" notation syntax?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: No, Python does not have a `..` notation syntax, and `1..\_\_truediv\_\_` is not a valid expression.
---

**Contents**

[TOC]

Background
----------

Python has a range object that allows us to generate a sequence of integers. A `range` object can be created by passing a `start`, `stop`, and `step` argument. For example,

```python
r = range(1, 10, 2)
print(list(r)) # [1, 3, 5, 7, 9]
```

This creates a `range` object that starts from 1 and generates values up to (but not including) 10 in steps of 2.

Dot dot notation
----------------

One interesting feature of Python is the `..` (dot dot) notation, which is used in some contexts to create ranges of values. For example,

```python
r = 1..10
print(r) # SyntaxError: invalid syntax
```

This code produces a syntax error because Python does not recognize the `..` notation. However, we can make use of the `range` function to achieve the same result:

```python
r = range(1, 11)
print(list(r)) # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

This code creates a `range` object that starts from 1 and generates values up to (but not including) 11. By passing the `range` object to the `list` function, we convert it to a list of integers.


`__truediv__`
-------------

The code `1..__truediv__` is an attempt to call the `__truediv__` method of the `float` class on the `1` integer literal. However, this code produces a `SyntaxError` because of the invalid `..` notation.

If we want to divide the `1` integer by a floating-point value, we can simply use the `/` operator:

```python
result = 1 / 3.0
print(result) # 0.3333333333333333
```

This code divides the `1` integer by `3.0` (a floating-point value), resulting in a floating-point number. The result is assigned to the `result` variable and printed to the console.
