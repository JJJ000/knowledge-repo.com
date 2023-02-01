---
title: Regular expression without re.compile that is not case sensitive?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the re.search function with the re.IGNORECASE flag set to perform a case insensitive regular expression.
---

**Contents**

[TOC]

### Using re.search

The re.search function can be used to perform case insensitive regular expression searches without using re.compile. This is done by using the re.IGNORECASE flag when calling re.search.

Example:

```python
import re

string = "This is a string"

match = re.search(r'this', string, re.IGNORECASE)

if match:
    print("Match found:", match.group())
```

### Using re.findall

The re.findall function can also be used to perform case insensitive regular expression searches without using re.compile. This is done by using the re.IGNORECASE flag when calling re.findall.

Example:

```python
import re

string = "This is a string"

matches = re.findall(r'this', string, re.IGNORECASE)

if matches:
    print("Matches found:", matches)
```

### Using re.sub

The re.sub function can be used to perform case insensitive regular expression searches without using re.compile. This is done by using the re.IGNORECASE flag when calling re.sub.

Example:

```python
import re

string = "This is a string"

new_string = re.sub(r'this', 'that', string, flags=re.IGNORECASE)

print("New string:", new_string)
```

### Using re.split

The re.split function can also be used to perform case insensitive regular expression searches without using re.compile. This is done by using the re.IGNORECASE flag when calling re.split.

Example:

```python
import re

string = "This is a string"

split_string = re.split(r'this', string, flags=re.IGNORECASE)

print("Split string:", split_string)
```
