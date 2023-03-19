---
title: Python code for interpreting a binary file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can read a binary file with Python using the built-in function `open()` with the mode ``rb``.
---

**Contents**

[TOC]

## Introduction
Binary file reading is an essential part of data I/O, especially in fields like computer vision, machine learning, and robotics. This article explains how to read binary files in Python.

## Using Python's built-in `open()` function 
Python provides a built-in `open()` function to read files. It opens files in text mode by default, but you can also specify it to open a file in binary mode. Here is how you can read a binary file using the `open()` function:

```python
with open('binary_file', 'rb') as f:
   byte = f.read(1)
   while byte != b'':
       # Do something with the read byte
       byte = f.read(1)
``` 

In this example, we read one byte each time and do something with it in each iteration. Note that we read one byte at a time because we are dealing with a binary file. If you are dealing with a text file, you can read the file line by line using the `readlines()` function.

## Using NumPy
NumPy is a widely used numerical computing library in the Python ecosystem. It provides efficient array operations and data structures. NumPy also provides an easy-to-use method to read binary files through `np.fromfile()` and `np.memmap()`. Below is example code for using `np.fromfile()` to read in a binary file:

```python
import numpy as np

binary_data = np.fromfile('binary_file', dtype=np.uint8)
```

After running this code, the binary data is loaded into a NumPy array. Note that we specify the `dtype` to be `uint8` (unsigned 8-bit integer), but you can also use other data types as well, such as `int16`, `float32`, etc.

## Using `struct` module
Another way to read binary files in Python is by using the `struct` module. The `struct` module provides methods to pack and unpack data in binary format. It supports a wide range of data types and structures. Here is an example of how to use the `struct` module to read binary data:

```python
import struct

with open('binary_file', 'rb') as f:
   byte = f.read(4)
   while byte != b'':
       # Read a float (4-byte)
       value = struct.unpack('f', byte)[0]
       # Do something with the read value
       byte = f.read(4)
```

In this example, we read 4 bytes (one float value) each time with `f.read(4)` and unpack it with `struct.unpack('f', byte)[0]` which returns a float value. We can then do something with the read value in each iteration. Note that the `struct` module requires you to specify the data type and size, which might be a bit more difficult to use than the previous methods. However, it gives you more flexibility and control over how to read and pack data. 

## Conclusion
In summary, reading binary files in Python has various methods one can effectively use, using python's open() function, using NumPy, and using the struct module. Each method has its advantages and disadvantages. One can choose which method to use based on their requirements and the type of binary file they are dealing with.
