---
title: Replace multiple consecutive whitespace characters with a single whitespace in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Python`s `re` module can be used to substitute multiple whitespace characters with a single whitespace character using the regex `\s+` and the `sub` method.
---

**Contents**

[TOC]

### Using Regex

Python's `re` module provides a function called `sub` that can be used to substitute multiple whitespace with single whitespace.

```python
import re

string = "This    is    a   string    with    multiple    whitespace"

# Replace multiple whitespace with single whitespace
string = re.sub('\s+', ' ', string)

print(string)
# Output: This is a string with multiple whitespace
```

### Using String Method

The `replace` method of a string can also be used to substitute multiple whitespace with single whitespace.

```python
string = "This    is    a   string    with    multiple    whitespace"

# Replace multiple whitespace with single whitespace
string = string.replace('  ', ' ')

print(string)
# Output: This is a string with multiple whitespace
```
