---
title: Attributeerror 'str' object has no attribute 'decode' in Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The `str` object in Python 3 does not have the `decode` attribute, as strings are already stored as Unicode in Python 3.
---

**Contents**

[TOC]

# Overview
The `str` object has no attribute `decode` error is a common Python 3 error that occurs when attempting to decode a string object. This error is caused by attempting to decode a string object in Python 3, which does not support the `decode` method.

# Cause
In Python 3, the `str` object does not have a `decode` method. This is because in Python 3, strings are stored as Unicode by default, so there is no need to decode them.

# Solution
To solve this error, you should use the `bytes.decode()` method instead of the `str.decode()` method. The `bytes.decode()` method takes a bytes object as an argument and returns a string object.

# Example
For example, if you want to decode a string object in Python 3, you can use the following code:

```
my_string = b"Hello World!"
decoded_string = my_string.decode()
print(decoded_string)
```

The output of this code will be:

```
Hello World!
```
