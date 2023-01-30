---
title: What is the best way to remove whitespace?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the string method strip() to remove leading and trailing whitespace from a string.
---

**Contents**

[TOC]

#### Using the `str.strip()` Method
The `str.strip()` method can be used to trim whitespace from a string. This method removes any leading and trailing whitespace characters (spaces, tabs, and newlines) from the given string and returns a new string.

For example:

```python
my_string = "   Hello world!   "
print(my_string.strip())  # Outputs "Hello world!"
```

#### Using the `str.lstrip()` and `str.rstrip()` Methods
The `str.lstrip()` and `str.rstrip()` methods can be used to trim whitespace from the left and right sides of a string, respectively. These methods remove any leading and trailing whitespace characters (spaces, tabs, and newlines) from the given string and return a new string.

For example:

```python
my_string = "   Hello world!   "
print(my_string.lstrip())  # Outputs "Hello world!   "
print(my_string.rstrip())  # Outputs "   Hello world!"
```

#### Using the `re.sub()` Method
The `re.sub()` method can be used to trim whitespace from a string using regular expressions. This method can be used to remove all leading and trailing whitespace characters (spaces, tabs, and newlines) from the given string and returns a new string.

For example:

```python
import re
my_string = "   Hello world!   "
print(re.sub(r"^\s+|\s+$", "", my_string))  # Outputs "Hello world!"
```

#### Using the `string.whitespace` Constant
The `string.whitespace` constant can be used to trim whitespace from a string. This constant contains a list of all the whitespace characters (spaces, tabs, and newlines) that can be used to remove any leading and trailing whitespace characters from the given string and return a new string.

For example:

```python
import string
my_string = "   Hello world!   "
for char in string.whitespace:
    my_string = my_string.replace(char, "")
print(my_string)  # Outputs "Hello world!"
```
