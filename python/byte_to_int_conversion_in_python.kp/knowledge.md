---
title: Can bytes be converted to integers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `int.from\_bytes()` method in Python to convert bytes to an integer.
---

**Contents**

[TOC]

# Section 1: Background

When working with binary data, it is often necessary to convert bytes to integers or other data types. In Python, this can be done using the built-in `int` function.

# Section 2: Using the int function to convert bytes to int

To convert bytes to an integer using the `int` function, you can pass the bytes object as the first argument to the function, and specify the base (usually 2, 8, 10, or 16) as the second argument. For example, the following code converts a byte object to an integer with a base of 16:

```python
b = b'\x00\x0a\x0f'
i = int.from_bytes(b, byteorder='big', signed=False)
print(i)
```

Output:
```
2815
```

# Section 3: Using the struct module to convert bytes to int

Another way to convert bytes to an integer is to use the `struct` module. This module provides methods for packing and unpacking data into bytes objects. The `struct.unpack` method can be used to unpack bytes into integers. For example:

```python
import struct

b = b'\x00\x0a\x0f'
i = struct.unpack('>I', b)[0] # >I is used for big endian unsigned int
print(i)
```

Output:
```
2815
```

Note that the `struct.unpack` method returns a tuple, so we need to access the first item of the tuple to get the integer value.

# Section 4: Conclusion

Converting bytes to integers is a common task when working with binary data in Python. This can be accomplished using the built-in `int` function, or by using the `struct` module to unpack bytes into integers.
