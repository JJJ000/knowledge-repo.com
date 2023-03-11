---
title: Convert a string into a series of hexadecimal bytes and display the output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To print a string as hexadecimal bytes in Python, use the `.encode(`hex`)` method.
---

**Contents**

[TOC]

# Introduction
In Python, you can convert a string to a sequence of bytes or a sequence of integers representing the Unicode code points of the characters in the string. Then, you can encode the bytes in a hexadecimal format to obtain a hexadecimal representation of the string.

# Converting a string to bytes
To convert a string to bytes in Python, you can use the `bytes` or `bytearray` function, which take a string and an encoding as arguments. The encoding specifies the character encoding used to map the characters in the string to bytes.

For example, to convert the string "hello" to bytes using the UTF-8 encoding, you can do:

```
string = "hello"
bytes = string.encode("utf-8")
```

# Encoding bytes in hexadecimal
To encode the bytes in a hexadecimal format, you can use the `binascii` module, which provides several functions for converting binary data to and from different representations, including hexadecimal.

To convert the bytes to a hexadecimal string, you can use the `binascii.hexlify` function, which takes a byte string as argument and returns a byte string containing the hexadecimal representation of the input.

For example, to encode the bytes obtained from the previous section in hexadecimal, you can do:

```
import binascii

hex = binascii.hexlify(bytes)
```

# Printing the hexadecimal string
To print the hexadecimal string, you can convert it to a regular string using the `decode` method of the byte string.

For example, to print the hexadecimal string obtained from the previous section, you can do:

```
print(hex.decode("utf-8"))
```

This will print the string "68656c6c6f" to the console.
