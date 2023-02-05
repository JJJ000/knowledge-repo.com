---
title: Split a string by spaces while maintaining any quoted substrings in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the shlex.split() function to split a string by spaces while preserving quoted substrings in Python.
---

**Contents**

[TOC]

**Section 1: Importing Libraries**

```python
import re
```

**Section 2: Defining Function**

```python
def split_by_spaces_preserving_quotes(string):
    return re.findall(r'(?:[^\s"]|"(?:\\.|[^"])*")+', string)
```

**Section 3: Example Usage**

```python
my_string = 'This is a "string with spaces" inside quotes'
split_string = split_by_spaces_preserving_quotes(my_string)

# split_string = ['This', 'is', 'a', '"string with spaces"', 'inside', 'quotes']
```

**Section 4: Explanation**

The function `split_by_spaces_preserving_quotes()` uses a regular expression to find all substrings that are either not whitespace or enclosed in double quotes. This allows the function to split the string by spaces while preserving any substrings that are enclosed in quotes.
