---
title: What is the complete file path of the directory containing the current file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The full path of the current file`s directory can be obtained using the os.path.dirname() function.
---

**Contents**

[TOC]

## Using os.path

The `os.path` module in the Python standard library provides several functions to manipulate path names. To get the full path of the current file's directory, you can use the `os.path.dirname()` function.

```python
import os

# Get the current file's directory
current_directory = os.path.dirname(os.path.abspath(__file__))

print(current_directory)
```

## Using pathlib

The `pathlib` module in the Python standard library provides an object-oriented approach to manipulating path names. To get the full path of the current file's directory, you can use the `Path.cwd()` method.

```python
from pathlib import Path

# Get the current file's directory
current_directory = Path.cwd()

print(current_directory)
```
