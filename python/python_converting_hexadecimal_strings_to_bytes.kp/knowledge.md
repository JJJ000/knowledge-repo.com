---
title: What is the method for converting a hexadecimal string into bytes using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the bytes.fromhex() method to convert a hexadecimal string to bytes in Python.
---

**Contents**

[TOC]

## Introduction
In Python, you can convert a hexadecimal string to bytes using built-in methods. In this tutorial, we will cover the various methods available to convert a hexadecimal string to bytes.

## Using the bytearray() Function
The `bytearray()` function returns an array of bytes. You can pass a hexadecimal string to this function, and it will return a byte array.

```python
hex_string = "68656c6c6f" # hexadecimal string
bytes_array = bytearray.fromhex(hex_string) # convert to byte array
print(bytes_array) # b'hello'
```

## Using the bytes() Function
The `bytes()` function also returns an array of bytes. You can pass a hexadecimal string to this function, and it will return a byte array.

```python
hex_string = "68656c6c6f" # hexadecimal string
bytes_array = bytes.fromhex(hex_string) # convert to byte array
print(bytes_array) # b'hello'
```

## Using the binascii Module
The `binascii` module in Python has various methods to convert hexadecimal strings to bytes. The `unhexlify()` function from the `binascii` module returns the corresponding bytes of a hexadecimal string.

```python
import binascii

hex_string = "68656c6c6f" # hexadecimal string
bytes_array = binascii.unhexlify(hex_string) # convert to byte array
print(bytes_array) # b'hello'
```

## Using the codecs Module
The `codecs` module provides various codecs to encode and decode data. The `hex_codec` codec can be used to decode a hexadecimal string to bytes.

```python
import codecs

hex_string = "68656c6c6f" # hexadecimal string
bytes_array = codecs.decode(hex_string, "hex_codec") # convert to byte array
print(bytes_array) # b'hello'
```

## Conclusion
In this tutorial, we covered various methods to convert a hexadecimal string to bytes in Python. Using any of these methods, you can easily convert a hexadecimal string to bytes.
