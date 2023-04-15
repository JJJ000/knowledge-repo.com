---
title: How to translate bytes into a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Bytes can be converted to a string in Python using the `decode()` method.
---

**Contents**

[TOC]

### Using `str()`
The `str()` function can be used to convert bytes to a string. It takes one argument, which is the bytes object to be converted, and returns the corresponding string.

Example:
```python
# bytes object
b = b'Hello World'

# convert bytes to string
s = str(b)

print(s)
# Output: 'Hello World'
```

### Using `decode()`
The `decode()` method can be used to convert bytes to a string. It takes one argument, which is the encoding type, and returns the corresponding string.

Example:
```python
# bytes object
b = b'Hello World'

# convert bytes to string
s = b.decode('utf-8')

print(s)
# Output: 'Hello World'
```

### Using `bytes.decode()`
The `bytes.decode()` method can also be used to convert bytes to a string. It takes one argument, which is the encoding type, and returns the corresponding string.

Example:
```python
# bytes object
b = b'Hello World'

# convert bytes to string
s = bytes.decode(b, 'utf-8')

print(s)
# Output: 'Hello World'
```
