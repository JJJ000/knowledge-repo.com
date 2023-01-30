---
title: When handling file content in Python 3, an object of type 'bytes' is required, not a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: A bytes object is required instead of a string object when handling file content in Python 3.
---

**Contents**

[TOC]

# Introduction
When handling file content in Python 3, it is possible to encounter a TypeError that reads "a bytes-like object is required, not 'str'". This error occurs when attempting to read a file using the `open()` function and specifying the `encoding` parameter as a string. 

# What Causes the Error
The `open()` function requires a `bytes-like object` as the `encoding` parameter, not a string. This means that the `encoding` parameter should be a byte sequence, such as a `bytes` object or a `bytearray`. 

# How to Fix the Error
To fix this error, the `encoding` parameter should be specified as a `bytes-like object` instead of a string. The following example shows how to do this:

```python
# Open the file with the specified encoding
with open('my_file.txt', 'r', encoding=bytes('utf-8', 'utf-8')) as f:
    # Read the file content
    content = f.read()
```

# Conclusion
It is important to remember that when handling file content in Python 3, the `encoding` parameter of the `open()` function should be specified as a `bytes-like object`, not a string. Otherwise, a TypeError will occur.
