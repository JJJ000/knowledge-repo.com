---
title: Reword the sentence "how to print bytes in Python 3 without the prefix 'b'"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use `.decode()` to convert bytes to string and print without the b` prefix.
---

**Contents**

[TOC]

Introduction
------------
In Python 3, when we convert a string to bytes using the `encode()` method, it returns a bytes object. When we try to print this bytes object, it is displayed with a prefix `b'` to indicate that it is a bytes object. However, sometimes we may want to print the bytes object without this prefix. In this article, we will see how we can print bytes without the prefix in Python 3.

Method 1: Using the decode() method
----------------------------------
The simplest and most efficient way to print bytes without the prefix `b'` is to use the `decode()` method. This method converts the bytes object to a string object. We can then print the string using the `print()` statement. Here's an example:

```python
>>> byte_string = b'Hello, World!'
>>> print(byte_string.decode())
Hello, World!
```

In the above code, we first create a bytes object `byte_string`. We then call the `decode()` method on it to convert it to a string, and finally print it using the `print()` statement. Note that the `decode()` method can take an argument that specifies the encoding of the bytes. If the encoding is not specified, it defaults to `utf-8`.

Method 2: Using the str() constructor
--------------------------------------
Another way to print bytes without the prefix `b'` is to convert the bytes object to a string object using the `str()` constructor. Here's an example:

```python
>>> byte_string = b'Hello, World!'
>>> print(str(byte_string, 'utf-8'))
Hello, World!
```

In the above code, we use the `str()` constructor to convert the bytes object to a string object. The `str()` constructor takes two arguments: the first argument is the bytes object, and the second argument is the encoding of the bytes. We then print the string using the `print()` statement.

Method 3: Using the bytes() constructor
----------------------------------------
Another way to print bytes without the prefix `b'` is to create a new bytes object using the `bytes()` constructor. Here's an example:

```python
>>> byte_string = b'Hello, World!'
>>> print(bytes(byte_string).decode('utf-8'))
Hello, World!
```

In the above code, we create a new bytes object using the `bytes()` constructor. The `bytes()` constructor takes a bytes object as an argument, and returns a new bytes object that is a copy of the original bytes object. We then call the `decode()` method on the new bytes object to convert it to a string, and finally print it using the `print()` statement.

Conclusion
----------
In this article, we saw three different ways to print bytes without the prefix `b'` in Python 3. We can either use the `decode()` method, the `str()` constructor, or create a new bytes object using the `bytes()` constructor. All three methods are simple and efficient, and can be used depending on the requirements of the program.
