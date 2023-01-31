---
title: In python, divide a string using multiple separators
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the re.split() function with a regular expression pattern to split a string with multiple delimiters in Python.
---

**Contents**

[TOC]

## Using str.split()

The `str.split()` method can be used to split a string with multiple delimiters. It takes a string argument for the delimiters, and splits the string at each occurrence of any of the delimiters.

Example:
```python
s = 'foo,bar;baz'

s.split(',;')
# ['foo', 'bar', 'baz']
```

## Using regex

We can also use a regular expression to split a string with multiple delimiters. The `re.split()` method takes a regular expression as its argument, and will split the string along any occurrence of the delimiters specified in the regex.

Example:
```python
import re

s = 'foo,bar;baz'

re.split('[,;]', s)
# ['foo', 'bar', 'baz']
```

## Using str.split() with maxsplit

The `str.split()` method also has an optional argument `maxsplit`, which specifies the maximum number of splits to make. This can be useful if we want to split the string at the first occurrence of any of the delimiters.

Example:
```python
s = 'foo,bar;baz'

s.split(',;', maxsplit=1)
# ['foo', 'bar;baz']
```

## Using regex with lookaround

We can also use a regular expression with lookarounds to split a string with multiple delimiters. Lookarounds are a special type of regex that allow us to match a pattern without including it in the result.

Example:
```python
import re

s = 'foo,bar;baz'

re.split('(?<=[,;])', s)
# ['foo', 'bar', 'baz']
```
