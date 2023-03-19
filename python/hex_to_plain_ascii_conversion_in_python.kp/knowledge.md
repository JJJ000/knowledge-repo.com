---
title: How to transform a hex-encoded ascii string to plain ascii?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the decode() method with the `hex` encoding parameter to convert the Hex string to plain ASCII string in Python.
---

**Contents**

[TOC]

## Introduction

In this tutorial, we will learn how to convert ASCII strings encoded in hex to plain ASCII strings in Python. This tutorial is useful for anyone who is working with data encoded in hex and wants to convert it back to the original ASCII string.

## Prerequisites

Before we get started, you need to have Python installed on your computer. You can download and install it from the official website: [https://www.python.org/downloads/](https://www.python.org/downloads/).

## Converting Hex to ASCII

To convert a hex string to an ASCII string, we can use the `bytes.fromhex` method in Python. This method takes a hex string and returns a bytes object. We can then convert the bytes object to a string using the `decode` method.

Here’s an example:

```python
hex_string = "48656c6c6f20576f726c64"
ascii_string = bytes.fromhex(hex_string).decode('utf-8')
print(ascii_string)
```

Output:
```
Hello World
```

## Converting Hex to ASCII using binascii

Another way to convert hex strings to ASCII strings is to use the `binascii` module in Python. This module provides a `unhexlify` function that takes a hex string and returns the corresponding bytes object.

Here’s an example:

```python
import binascii

hex_string = "48656c6c6f20576f726c64"
bytes_object = binascii.unhexlify(hex_string)
ascii_string = bytes_object.decode('utf-8')

print(ascii_string)
```

Output:
```
Hello World
```

## Conclusion

In this tutorial, we learned how to convert ASCII strings encoded in hex to plain ASCII strings in Python. We saw two methods: one using the `bytes.fromhex` method and another using the `unhexlify` function from the `binascii` module. Both methods work well, and you can choose the one that suits you best.
