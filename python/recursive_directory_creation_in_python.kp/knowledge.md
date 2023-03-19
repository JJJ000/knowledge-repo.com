---
title: What is the method for recursively creating directories?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the os.makedirs() function to create directories recursively in Python.
---

**Contents**

[TOC]

## Introduction
In Python, you can create directories recursively using the `os.makedirs()` function. This function creates a directory and any necessary parent directories.

## Basic Usage
Here's an example of using `os.makedirs()` to create a directory and subdirectory recursively:

```python
import os

os.makedirs("path/to/directory")
```

This code will create a directory called "directory" inside the "to" directory, which is itself inside the "path" directory.

## Handling Exceptions
If you need to handle errors that might arise when creating directories, you can wrap the call to `os.makedirs()` in a try-except block:

```python
import os

try:
    os.makedirs("path/to/directory")
except OSError as e:
    print("Error: %s - %s." % (e.filename, e.strerror))
```

In this code, if an `OSError` occurs (for example, if the directory already exists or there is a permission error), the script will print an error message that includes the filename and the error message.

## Using Recursive Flag
Another way to create directories recursively is to use the `exist_ok` flag in `os.makedirs()`. Set this flag to `True` to avoid raising an exception if the directory already exists:

```python
import os

os.makedirs("path/to/directory", exist_ok=True)
```

This will create the directory "directory" inside the "to" directory, which is inside the "path" directory, without raising an exception if the directory already exists.
