---
title: What is the interval for dividing a string into parts?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the [string[ii+n] for I in range(0, len(string), n)] syntax to split a string every nth character in Python.
---

**Contents**

[TOC]

### Using `str.slice`

The `str.slice` method can be used to split a string every nth character. The syntax for `str.slice` is `str.slice(start, end)`, where `start` is the index of the first character to include in the slice, and `end` is the index of the character after the last character to include in the slice.

For example, to split a string `str` every 3rd character, the following code can be used:

```python
for i in range(0, len(str), 3):
    print(str[i:i+3])
```

### Using `str.split`

The `str.split` method can also be used to split a string every nth character. This method takes a delimiter as a parameter and splits the string into a list of strings based on the delimiter.

For example, to split a string `str` every 3rd character, the following code can be used:

```python
for i in range(0, len(str), 3):
    print(''.join(str.split(str[i:i+3])))
```

### Using `re.split`

The `re.split` method from the `re` module can also be used to split a string every nth character. This method takes a regular expression as a parameter and splits the string into a list of strings based on the regular expression.

For example, to split a string `str` every 3rd character, the following code can be used:

```python
import re

for i in range(0, len(str), 3):
    print(''.join(re.split(str[i:i+3], str)))
```

### Using `itertools.islice`

The `itertools.islice` method from the `itertools` module can also be used to split a string every nth character. This method takes a start and an end index as parameters and returns an iterator over the slice of the string between the start and end indices.

For example, to split a string `str` every 3rd character, the following code can be used:

```python
from itertools import islice

for i in range(0, len(str), 3):
    print(''.join(islice(str, i, i+3)))
```
