---
title: Take off the initial characters from a given string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can remove a prefix from a string in Python using the built-in function `lstrip()`.
---

**Contents**

[TOC]

Section 1: Introduction
Python is a popular programming language that provides several built-in methods for manipulating strings. The prefix of a string is a sequence of characters at the beginning of the string. In some cases, we may want to remove a prefix from a string to obtain the remaining part of the string. In this tutorial, we will see how to remove a prefix from a string in Python.

Section 2: Using the removeprefix() method
Starting from Python 3.9, a new built-in method called removeprefix() has been added to the str class. This method takes a prefix as an argument and removes it from the beginning of the string if it exists. If the prefix does not exist in the string, the method returns the original string.

Here's an example:

```python
# Using the removeprefix() method
string = "Hello world"
prefix = "Hello "
result = string.removeprefix(prefix)
print(result)  # Output: "world"
```
In the example above, we have a string "Hello world" and a prefix "Hello ". We use the removeprefix() method to remove the prefix from the string and obtain the result "world".

Section 3: Using slicing
If you are using an older version of Python that does not support the removeprefix() method, you can use slicing to remove a prefix from a string. Slicing is a way to extract a part of a string by specifying its start and end indices.

Here's an example:

```python
# Using slicing
string = "Hello world"
prefix = "Hello "
result = string[len(prefix):]
print(result)  # Output: "world"
```
In the example above, we use slicing to extract the part of the string that comes after the prefix. The len() function is used to get the length of the prefix, which is then used as the start index of the slice.

Section 4: Conclusion
In this tutorial, we have seen how to remove a prefix from a string in Python using the removeprefix() method and slicing. The removeprefix() method is a more concise and readable way to remove a prefix, but it is only available in Python 3.9 or later. If you are using an older version of Python, you can use slicing to achieve the same result.
