---
title: What is the process of transforming a sequence of bytes to an integer?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `int.from\_bytes(bytes, byteorder)` method to convert a string of bytes into an int in Python.
---

**Contents**

[TOC]

Converting String to bytes 

The first step to convert a string of bytes into an int in Python is to convert the string into bytes. The string can be converted into bytes using the `encode()` function in Python. 

```
string = "Hello World!"
byte_string = string.encode()
```

This will encode the string into bytes and return a byte-string object called `byte_string`.

Converting Bytes to Integer 

The next step is to convert the byte string into an integer. This can be done using the `int.from_bytes()` function in Python. 

```
int_val = int.from_bytes(byte_string, byteorder='big')
```

The `int.from_bytes()` function takes in two arguments, the `byte_string` and the `byteorder`. In this case, we specify the byte-order to be `'big'`, which means that the most significant byte comes first. 

Note that the value of `int_val` will be a large number because the byte-string for `"Hello World!"` is quite long. 

Converting Int to Smaller Integers

If the result is larger than the maximum size of the integer type that you want, then you can use the modulus operator to get a smaller number. 

```
int_val = int_val % (2 ** 32)
```

In this code, we are getting the remainder of the `int_val` divided by `2 ** 32`. This will give us a number that fits within an unsigned 32-bit integer. 

Alternatively, you can use the modulo operator to get a number between 0 and 255, which can be stored in a single byte. 

```
byte_val = int_val % 256
```

This will give you the byte value of the original byte-string.
