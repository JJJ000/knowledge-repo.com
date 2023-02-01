---
title: What is the process for dividing a string into separate words?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the split() method on the string to create a list of words.
---

**Contents**

[TOC]

1. Using `split()` Function:

The `split()` function is used to split strings into a list of words. It takes an optional parameter `sep` which specifies the delimiter to use when splitting the string. By default, the `split()` function uses whitespace as the delimiter.

```python
string = "This is a string"

words = string.split()

print(words)
# Output: ['This', 'is', 'a', 'string']
```

2. Using `re.split()` Function:

The `re.split()` function is used to split strings using a regular expression. It takes two parameters: `pattern` and `string`. The `pattern` parameter is a regular expression that defines the delimiter to use when splitting the `string`.

```python
import re

string = "This is a string"

words = re.split("\s+", string)

print(words)
# Output: ['This', 'is', 'a', 'string']
```

3. Using `shlex.split()` Function:

The `shlex.split()` function is used to split strings into a list of words, taking into account any quoted strings within the string. It takes one parameter `string`, which is the string to be split.

```python
import shlex

string = "This is a 'quoted string'"

words = shlex.split(string)

print(words)
# Output: ['This', 'is', 'a', 'quoted string']
```

4. Using `str.splitlines()` Function:

The `str.splitlines()` function is used to split a string into a list of lines. It takes an optional parameter `keepends`, which is a boolean value indicating whether the newline characters should be included in the resulting list.

```python
string = "This is\na string"

lines = string.splitlines(keepends=True)

print(lines)
# Output: ['This is\n', 'a string']
```
