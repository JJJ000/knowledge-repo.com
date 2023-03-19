---
title: Determine whether the string solely comprises of whitespace characters
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the isspace() method to check if a string contains only whitespace in Python.
---

**Contents**

[TOC]

## Approach 1: Using `isspace()` method

The `isspace()` method returns True if all the characters in a string are whitespace characters. We can utilize this method to check whether a string contains only whitespace or not.


```python
# function to check if string contains only whitespace
def check_whitespace(s):
    if s.isspace():
        return True
    return False
```

## Approach 2: Using Regular expression

We can use the `re.search()` method to check if the string contains only whitespace characters using a regular expression pattern.

```python
import re

# function to check if string contains only whitespace
def check_whitespace_re(s):
    pattern = '^\s*$'
    if re.search(pattern, s):
        return True
    return False
```

## Approach 3: Using `all()` method

Another approach is to apply the `isspace()` method on each character in the string and check if all the characters are whitespace.

```python
# function to check if string contains only whitespace
def check_whitespace_all(s):
    if all(char.isspace() for char in s):
        return True
    return False
```

## Example and Output

```python
s = '   '
print(check_whitespace(s))   # True
print(check_whitespace_re(s))   # True
print(check_whitespace_all(s))   # True

s = '   a'
print(check_whitespace(s))   # False
print(check_whitespace_re(s))   # False
print(check_whitespace_all(s))   # False
```

Output:

```
True
True
True
False
False
False
```
