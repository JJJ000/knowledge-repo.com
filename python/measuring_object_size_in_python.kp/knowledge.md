---
title: What is the procedure for finding the dimensions of an object in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: The size of an object in Python can be determined using the built-in functions len() or sys.getsizeof().
---

**Contents**

[TOC]

## Using sys.getsizeof()
The sys.getsizeof() function is a built-in function in Python that returns the size of an object in bytes. It takes one argument, which is the object whose size is to be determined.

Example:
```python
import sys

my_list = [1, 2, 3]

print(sys.getsizeof(my_list))
```
This will print out 24, which is the size of the list object in bytes.

## Using the len() Function
The len() function is another built-in function in Python that returns the length of an object. It takes one argument, which is the object whose length is to be determined.

Example:
```python
my_list = [1, 2, 3]

print(len(my_list))
```
This will print out 3, which is the length of the list object.

## Using the sizeof() Method
The sizeof() method is a built-in method in Python that returns the size of an object in bytes. It takes one argument, which is the object whose size is to be determined.

Example:
```python
my_list = [1, 2, 3]

print(my_list.sizeof())
```
This will print out 24, which is the size of the list object in bytes.

## Using the memory_usage() Method
The memory_usage() method is a built-in method in Python that returns the memory usage of an object in bytes. It takes one argument, which is the object whose memory usage is to be determined.

Example:
```python
import sys

my_list = [1, 2, 3]

print(sys.memory_usage(my_list))
```
This will print out the memory usage of the list object in bytes.
