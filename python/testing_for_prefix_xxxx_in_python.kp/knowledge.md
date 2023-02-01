---
title: Determining if a string begins with xxxx
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, you can use the startswith() method to check if a string starts with a given substring.
---

**Contents**

[TOC]

## Using the `startswith()` Method

The `startswith()` method can be used to check whether a string starts with a certain substring. This method takes one or more strings as parameters and returns a boolean value (`True` or `False`).

Example:

```python
my_string = "XXXXHello World!"

result = my_string.startswith("XXXX")

print(result) # Output: True
```

## Using the `find()` Method

The `find()` method can also be used to check whether a string starts with a certain substring. This method takes one or more strings as parameters and returns the index of the beginning of the substring if it is found, or `-1` if it is not found.

Example:

```python
my_string = "XXXXHello World!"

result = my_string.find("XXXX")

print(result) # Output: 0
```

## Using Regular Expressions

Regular expressions can also be used to check whether a string starts with a certain substring. The `re.match()` method takes a regular expression pattern as the first argument and the string to search as the second argument. It returns a `Match` object if the substring is found, or `None` if it is not found.

Example:

```python
import re

my_string = "XXXXHello World!"

result = re.match("XXXX", my_string)

print(result) # Output: <re.Match object; span=(0, 4), match='XXXX'>
```
