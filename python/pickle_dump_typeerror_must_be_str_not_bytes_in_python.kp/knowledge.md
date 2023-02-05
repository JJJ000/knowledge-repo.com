---
title: Typeerror the argument to pickle.dump must be a string, not bytes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pickle.dump requires a string to be passed as an argument, not bytes.
---

**Contents**

[TOC]

# Overview

The `pickle.dump()` function is used to serialize objects, meaning it converts them into a byte stream. However, it only accepts a `str` type as its argument, not `bytes`. If a `bytes` type is passed, a `TypeError` will be raised.

# Causes

The `pickle.dump()` function only accepts a `str` type as its argument. This means that any other type, such as `bytes`, will cause the function to raise a `TypeError`.

# Solution

To avoid the `TypeError`, the `bytes` type should be converted to a `str` type before passing it to the `pickle.dump()` function. This can be done using the `str()` function.

# Example

The following example shows how to convert a `bytes` type to a `str` type before passing it to the `pickle.dump()` function.

```python
import pickle

# Create a bytes type
b = b'This is a bytes type'

# Convert the bytes type to a str type
s = str(b)

# Pass the str type to the pickle.dump() function
pickle.dump(s, open('test.p', 'wb'))
```
