---
title: How to write to a binary file in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `wb` flag when opening a file in Python to write in binary mode and the `write()` method to write data to the file.
---

**Contents**

[TOC]

# Introduction

Python provides a number of built-in functions and libraries to work with files. One common file type is binary files, which store data in binary format instead of human-readable text. In this tutorial, we will learn how to write to a binary file in Python.

# Writing to a Binary File using 'wb' mode

To write to a binary file in Python, we typically use the 'wb' mode. This mode opens the file for writing as a binary file. Here is an example of writing to a binary file:

```python
with open("example.bin", "wb") as file:
    file.write(b'\x00\xff\x12\x34')
```

In this example, we use the 'open' function to open the file "example.bin" in 'wb' mode. This creates a new binary file if the file doesn't already exist, or overwrites an existing file with the same name.

We then use the 'write' method of the file object to write binary data to the file. In this case, we write the bytes b'\x00\xff\x12\x34' to the file.

# Using Struct module to write structured data

If we want to write structured data to a binary file, we can use Python's 'struct' module. The 'struct' module provides functions for packing and unpacking binary data in a specific format. Here is an example of using the 'struct' module to write a Python tuple to a binary file:

```python
import struct

data = (1, 2.0, b"Hello, world!")
packed_data = struct.pack('If11s', *data)

with open("example.bin", "wb") as file:
    file.write(packed_data)
```

In this example, we first create a tuple 'data' containing an integer, a float, and a bytes object. We then use the 'pack' method of the 'struct' module to pack this tuple into a binary string in a specific format. The format string 'If11s' specifies that we want to pack an integer, a float, and an 11-byte string of bytes.

We then open the file "example.bin" in 'wb' mode and write the packed data to the file.

# Conclusion

In this tutorial, we learned how to write to a binary file in Python using the 'wb' mode and the 'struct' module. Writing to binary files is a useful skill when working with non-text data or when optimizing file I/O performance.
