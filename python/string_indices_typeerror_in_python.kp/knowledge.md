---
title: What is causing the error message 'typeerror string indices must be integers'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: This error occurs when attempting to access a character in a string using an index that is not an integer.
---

**Contents**

[TOC]

# What is a TypeError?
A TypeError is an error that occurs when you try to perform an operation on a data type that is not supported by that operation.

# What Causes a TypeError?
A TypeError is caused when you try to access a string using an index that is not an integer. Strings are a sequence of characters, and each character has an index position. To access the character at a certain index, you must use an integer.

# Example of a TypeError
For example, if you try to access a character in a string using a float, you will get a TypeError.

```
my_string = "Hello World"

# This will cause a TypeError
my_string[3.14]
```

# How to Fix a TypeError
To fix a TypeError, you must use an integer when accessing a string.

```
my_string = "Hello World"

# This will not cause a TypeError
my_string[3]
```
