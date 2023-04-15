---
title: What is the method to change a string into utf-8 format in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `encode()` method with the encoding set to UTF-8.
---

**Contents**

[TOC]

## Introduction

Unicode is a standard encoding scheme for computer processing of written texts in various scripts and languages. The utf-8 (Unicode Transformation Format, 8-bit) is a popular encoding format that enables the representation of a wide range of characters, including the non-Latin script. Python supports multiple built-in functions and modules to convert a string to utf-8 or any other encoding format.

## Using String.encode()

Python's String class provides an `encode()` method that returns a byte encoded version of the string using the specified encoding format. To convert a string to utf-8, we can use the `encode()` method with the "utf-8" encoding format.

```python
my_string = "Hello World!"
utf8_encoded_string = my_string.encode('utf-8')
print(utf8_encoded_string)
```

Output:
```
b'Hello World!'
```

The `encode()` method returns a bytes object, as indicated by the 'b' prefix.

## Using String.encodebytes()

In addition to the `encode()` method, Python also provides an `encodebytes()` method in the base64 module. This method returns a byte string representing the given string object in base64 encoding. To encode a string to utf-8 using `encodebytes()`, we need to first convert the string into bytes format, and then use the `encodebytes()` method.

```python
import base64

my_string = "Hello World!"
my_bytes = my_string.encode('utf-8')
utf8_encoded_string = base64.encodebytes(my_bytes)
print(utf8_encoded_string)
```

Output:
```
b'SGVsbG8gV29ybGQh\n'
```

The `encodebytes()` method returns a bytes object.

## Using the codecs Module

Python's `codecs` module provides methods for encoding and decoding a string from any valid encoding to any other encoding. To convert a string to utf-8 using `codecs`, we can use the `encode()` method with the "utf-8" encoding format.

```python
import codecs

my_string = "Hello World!"
utf8_encoded_string = codecs.encode(my_string, 'utf-8')
print(utf8_encoded_string)
```

Output:
```
b'Hello World!'
```

The `encode()` method returns a bytes object.

## Conclusion

In this tutorial, we covered the multiple built-in functions and methods available in Python to convert a string to utf-8. We explored the `encode()` and `encodebytes()` methods of the string class and the base64 module, respectively, in addition to the `encode()` method in the `codecs` module. With these conversion methods, we can easily work with various text inputs in different encoding formats in our Python programs.
