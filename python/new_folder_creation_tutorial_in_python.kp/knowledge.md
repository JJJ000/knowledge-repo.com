---
title: What are the steps for making a new folder?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the os module and the os.mkdir() function to create a new folder in Python.
---

**Contents**

[TOC]

## Introduction

In Python, we can create a new folder using the `os` and `path` modules. These modules provide a set of functions that allow us to interact with the file system.

## Creating a folder using os.mkdir()

The easiest way to create a new folder in Python is to use the `os.mkdir()` function. This function creates a new directory with the specified name.

```python
import os

# Name of the directory to be created
directory = "new_folder"

# Create the directory 
os.mkdir(directory)
```

## Creating a folder using pathlib.Path()

Python3 also introduced `pathlib` module to provide an object-oriented approach for working with the file system. The `Path` class provides methods for creating files and folders.

```python
from pathlib import Path

# Name of the directory to be created
directory = "new_folder"

# Create the directory 
Path(directory).mkdir(parents=True, exist_ok=True)
```

The `parent=True` parameter creates all the missing directories in the path. Whereas, the `exist_ok=True` parameter ensures the function doesn't raise an error if the directory already exists.

## Verifying folder creation

To verify the new folder creation, we can use the `os.path.exists()` function to check if the directory exists or not.

```python
import os

# Name of the directory to be created
directory = "new_folder"

# Create the directory 
os.mkdir(directory)

# Verify the directory exists
if os.path.exists(directory):
    print(f"{directory} exists")
else:
    print(f"{directory} doesn't exist")
```

## Conclusion

In conclusion, Python provides multiple ways to create a new folder in the file system. The `os.mkdir()` and `pathlib.Path()` methods provide a quick and easy way to create new folders in Python.
