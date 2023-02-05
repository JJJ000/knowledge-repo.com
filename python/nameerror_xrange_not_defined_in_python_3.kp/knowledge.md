---
title: Xrange() is not a valid function in Python 3; use range() instead
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python 3, xrange was replaced by the range function.
---

**Contents**

[TOC]

# Solution

## Overview

In Python 3, the `xrange` function has been removed and replaced with the `range` function. This means that any code written in Python 2 that uses `xrange` will cause a `NameError` when run in Python 3.

## Python 2

In Python 2, the `xrange` function is used to generate an iterable sequence of numbers. It is similar to the `range` function, but it returns an object that generates the numbers on demand, rather than generating all the numbers at once and storing them in memory. This makes it more efficient than `range` for large sequences of numbers.

## Python 3

In Python 3, the `xrange` function has been removed and replaced with the `range` function. The `range` function now behaves the same way that `xrange` did in Python 2, and it is now the preferred way to generate an iterable sequence of numbers in Python 3.

## Conclusion

When running Python 2 code in Python 3, any calls to `xrange` will cause a `NameError` as the function no longer exists. To fix this, the code needs to be updated to use the `range` function instead.
