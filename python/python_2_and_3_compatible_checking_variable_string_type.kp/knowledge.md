---
title: What is the method for verifying whether a variable is a string that is compatible with both Python 2 and 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use isinstance(variable, str) as it works in both Python 2 and 3.
---

**Contents**

[TOC]

# Determine the Data Type of a Variable

In Python, the built-in `type()` function can be used to determine the data type of a variable. However, depending on the version of Python being used, the output of `type()` for strings can vary.

# Python 2

In Python 2, the `type()` function returns `str` for ASCII strings and `unicode` for Unicode strings. To check if a variable is a string in Python 2, you can use the following code:

```python
if isinstance(my_var, basestring):
    # my_var is a string in Python 2
else:
    # my_var is not a string
```

The `isinstance()` function checks if `my_var` is an instance of the `basestring` class, which includes both `str` and `unicode` in Python 2.

# Python 3

In Python 3, there is no `basestring` class and all strings are Unicode strings. The `type()` function always returns `str` for strings in Python 3. To check if a variable is a string in Python 3, you can use the following code:

```python
if isinstance(my_var, str):
    # my_var is a string in Python 3
else:
    # my_var is not a string
```

The `isinstance()` function checks if `my_var` is an instance of the `str` class, which includes all strings in Python 3.

# Compatibility

To check if a variable is a string in both Python 2 and Python 3, you can use the following code:

```python
try:
    basestring
except NameError:
    basestring = str

if isinstance(my_var, basestring):
    # my_var is a string in Python 2 and Python 3
else:
    # my_var is not a string
```

This code first tries to access `basestring`, which is defined in Python 2 but not in Python 3. If `basestring` is not defined, it is set to `str`, which includes all strings in Python 3. The `isinstance()` function then checks if `my_var` is an instance of `basestring`, which includes both `str` and `unicode` in Python 2 and `str` in Python 3, making the code compatible with both versions of Python.
