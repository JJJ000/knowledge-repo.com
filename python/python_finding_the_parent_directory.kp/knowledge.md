---
title: What is the syntax to access the parent directory in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the os.path.dirname() function to get the parent directory in Python.
---

**Contents**

[TOC]

# Using os.path

The `os.path` module provides a number of useful functions for working with paths. The `os.path.dirname()` function can be used to get the parent directory of a given path.

Example:
```
import os

current_dir = os.getcwd()
parent_dir = os.path.dirname(current_dir)

print(parent_dir)
```

# Using os.pardir

The `os.pardir` constant can also be used to get the parent directory of a given path. This constant is a string representing the parent directory of the current directory.

Example:
```
import os

current_dir = os.getcwd()
parent_dir = os.path.join(current_dir, os.pardir)

print(parent_dir)
```

# Using pathlib

The `pathlib` module provides an object-oriented approach to working with paths. The `Path.parent` attribute can be used to get the parent directory of a given path.

Example:
```
from pathlib import Path

current_dir = Path.cwd()
parent_dir = current_dir.parent

print(parent_dir)
```
