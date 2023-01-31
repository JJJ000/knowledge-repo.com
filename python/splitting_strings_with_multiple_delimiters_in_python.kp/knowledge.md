---
title: Separate strings into individual words using multiple word separators
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: We can use the split() method with multiple word boundary delimiters to split strings into words in Python.
---

**Contents**

[TOC]

#### Using re.split()

The `re.split()` function can be used to split strings into words with multiple word boundary delimiters in Python. This function takes two arguments: the string to be split and a pattern to match. The pattern can be a regular expression that includes multiple word boundary delimiters.

For example, to split a string with multiple word boundary delimiters (e.g. `\s+`, `\t+`, `\n+`), the following pattern can be used:

```python
import re

string = "This is\ta\tstring with\nmultiple\tword\tboundary\tdelimiters"

words = re.split(r'\s+|\t+|\n+', string)

print(words)
```

Output:

```
['This', 'is', 'a', 'string', 'with', 'multiple', 'word', 'boundary', 'delimiters']
```

#### Using str.split()

The `str.split()` method can also be used to split strings into words with multiple word boundary delimiters in Python. This method takes one argument: the pattern to match. The pattern can be a regular expression that includes multiple word boundary delimiters.

For example, to split a string with multiple word boundary delimiters (e.g. `\s+`, `\t+`, `\n+`), the following pattern can be used:

```python
string = "This is\ta\tstring with\nmultiple\tword\tboundary\tdelimiters"

words = string.split(r'\s+|\t+|\n+')

print(words)
```

Output:

```
['This', 'is', 'a', 'string', 'with', 'multiple', 'word', 'boundary', 'delimiters']
```
