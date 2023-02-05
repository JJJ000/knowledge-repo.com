---
title: What is the process for converting a binary string to a regular string in python3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the str.encode() method to decode a binary string to a normal string in Python3.
---

**Contents**

[TOC]

# Section 1: Understand the Binary String
A binary string is a string of 0s and 1s that represent data in binary format. It is used to store and transfer data in computers, and is the basis of all digital data.

# Section 2: Convert the Binary String
In Python3, the easiest way to convert a binary string to a normal string is to use the `binascii` module. This module contains several functions that can be used to encode and decode binary data.

# Section 3: Using the binascii Module
To convert a binary string to a normal string, you can use the `binascii.unhexlify()` function. This function takes a binary string as an argument and returns a normal string.

# Section 4: Example
For example, let's say we have a binary string `0110100001100101011011000110110001101111`. We can use the `binascii.unhexlify()` function to convert this to a normal string:

```python
import binascii

binary_string = '0110100001100101011011000110110001101111'
normal_string = binascii.unhexlify(binary_string)
print(normal_string) # prints 'hello'
```
