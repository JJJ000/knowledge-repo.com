---
title: Eliminate all spaces in a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: ``.join(string.split())
---

**Contents**

[TOC]

# Using Regular Expressions

Regular expressions (regex) are a powerful tool for manipulating strings in Python. The following code snippet uses the `re.sub` function to remove all whitespace from a given string:

```python
import re

string = "This is a string with whitespace"

string_without_whitespace = re.sub(r'\s', '', string)

print(string_without_whitespace)
```

# Using str.replace

The `str.replace` method can also be used to remove all whitespace from a string. The following code snippet uses `str.replace` to achieve this:

```python
string = "This is a string with whitespace"

string_without_whitespace = string.replace(" ", "")

print(string_without_whitespace)
```

# Using List Comprehension

List comprehension is a powerful tool for manipulating lists in Python. The following code snippet uses list comprehension to remove all whitespace from a given string:

```python
string = "This is a string with whitespace"

string_without_whitespace = ''.join([c for c in string if c != ' '])

print(string_without_whitespace)
```

# Using str.join

The `str.join` method can also be used to remove all whitespace from a string. The following code snippet uses `str.join` to achieve this:

```python
string = "This is a string with whitespace"

string_without_whitespace = ''.join(s for s in string if s != ' ')

print(string_without_whitespace)
```
