---
title: Transforming a 'type' object in Python into a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the built-in str() function to convert a Python `type` object to a string.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, we often use the built-in function `type()` to get the type of a Python object. Sometimes it may be necessary to convert the `type` object to a string for further processing or display purposes.

Section 2: Using the str() Function
One way to convert a `type` object to a string is by simply passing it as an argument to the built-in `str()` function. Here's an example:

```python
# Check the type of a variable
x = 10
print(type(x))  # <class 'int'>

# Convert the type object to a string
type_str = str(type(x))
print(type_str)  # <class 'int'>
```

In this example, the `type()` function returns a `type` object (`<class 'int'>`) for the variable `x`. We then pass this object to the `str()` function to convert it to a string (`"<class 'int'>"`) and assign it to the variable `type_str`.

Section 3: Using the __name__ Attribute
Another way to convert a `type` object to its corresponding string representation is by accessing the `__name__` attribute of the object. Here's an example:

```python
# Check the type of a variable
x = 10
print(type(x))  # <class 'int'>

# Get the string representation of the type
type_str = type(x).__name__
print(type_str)  # int
```

In this example, we use the `__name__` attribute of the `type` object returned by the `type()` function to get the corresponding string representation (`"int"`) of the object.

Section 4: Conclusion
In Python, we can convert a `type` object to a string using either the `str()` function or the `__name__` attribute. Both methods are equally valid and effective, and the choice of which to use depends on personal preference and the specific use case.
