---
title: Ignore the multiple values returned by a Python function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, Python multiple return values should not be ignored as they are a useful way to return multiple values from a function.
---

**Contents**

[TOC]

# Ignoring Python Multiple Return Values

## Ignoring Values Directly
Python allows for multiple return values, which can be ignored directly. This is done by using a blank variable for the value that is to be ignored. For example:

```
def foo():
    return 1, 2

x, _ = foo()
```

In the example above, the second value returned by `foo()` is ignored by assigning it to the blank variable `_`.

## Using Unpacking
Python also allows for multiple return values to be ignored by using unpacking. Unpacking is a feature of Python that allows for a list of values to be assigned to multiple variables. For example:

```
def foo():
    return 1, 2

x, *_ = foo()
```

In the example above, the second value returned by `foo()` is ignored by assigning it to the blank variable `_` using unpacking.

## Ignoring the Return Value
Another way to ignore the return value of a function is to simply not assign it to any variable. For example:

```
def foo():
    return 1, 2

foo()
```

In the example above, the return value of `foo()` is ignored by not assigning it to any variable.

## Ignoring a Specific Value
Finally, Python allows for a specific value to be ignored from a multiple return value. This is done by using the `_` character in the variable name. For example:

```
def foo():
    return 1, 2

x, _2 = foo()
```

In the example above, the second value returned by `foo()` is ignored by assigning it to the variable `_2`.
