---
title: What is the best way to determine if a string is a numerical value (float or integer)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the `isnumeric()` or `isdecimal()` methods to check if a string represents a number in Python.
---

**Contents**

[TOC]

# Using Regular Expressions

Regular expressions are a powerful tool for matching patterns in strings. It can be used to check if a string represents a number (float or int) by using the pattern `\d+\.?\d*` which matches any sequence of digits with an optional decimal point and more digits.

# Using isdigit()

The `isdigit()` method can be used to check if a string is a digit. This method returns `True` if all characters in the string are digits and there is at least one character, `False` otherwise.

# Using isnumeric()

The `isnumeric()` method can be used to check if a string is numeric. This method returns `True` if all characters in the string are numeric characters, and there is at least one character, `False` otherwise.

# Using try/except

The `try/except` statement can be used to check if a string is a number. The `try` statement tries to convert the string to a `float` and if it succeeds, it returns `True`, otherwise it raises a `ValueError` exception which is caught by the `except` statement. If the `except` statement is reached, it means that the string is not a number and `False` is returned.
