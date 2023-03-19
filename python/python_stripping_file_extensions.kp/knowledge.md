---
title: What is the Python method for removing or replacing a file extension from a filename?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the `os.path.splitext()` function to split a filename and its extension, and then select the first part of the tuple to get the filename without the extension.
---

**Contents**

[TOC]

## Introduction

In Python, we can replace or strip an extension from a filename using various built-in functions.

## Using splitext() function

Python’s `os.path.splitext()` function splits the file path into its Filename and extension. We can use this function to get file name and extension, and then use string slicing to remove the extension.

Example:

```python
import os

# filename with extension
filename = "file.txt"

# split the file into filename and extension
name, ext = os.path.splitext(filename)

# print filename without extension
print(name)
```

Output:

```
file
```

## Using partition() function

Python’s `str.partition()` function splits a string in 3 parts: the part before the separator, the separator itself, and the part after the separator. We can use this function to split the filename by the `.` (dot) separator and separately handle the parts before and after the dot.

Example:

```python
# filename with extension
filename = "file.txt"

# split the file into filename and extension
name, _, ext = filename.partition(".")

# print filename without extension
print(name)
```

Output:

```
file
```

## Using rfind() and slicing

We can also use string slicing to remove the extension of the file. We can find the last `.` (dot) in the filename using the `str.rfind()` function and then slice the string to remove the extension.

Example:

```python
# filename with extension
filename = "file.txt"

# find the position of the last dot
dot_pos = filename.rfind(".")

# slice the filename to remove the extension
name = filename[:dot_pos]

# print filename without extension
print(name)
```

Output:

```
file
```

## Conclusion

In Python, we can use various built-in functions to replace or strip an extension from a filename. The `os.path.splitext()` function, `str.partition()` function, and `str.rfind()` function are some of the functions that we can use for this purpose. It is up to the user to choose the most suitable one for their specific use case.
