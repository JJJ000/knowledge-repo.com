---
title: What is the process for determining the size of a file in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: To check the file size in Python, use the os.path.getsize() function.
---

**Contents**

[TOC]

# Using os.path
The `os.path` module provides several methods to check the size of a file in Python.

## os.path.getsize()
The `os.path.getsize()` method returns the file size in bytes.

```python
import os

file_size = os.path.getsize("example.txt")
print("File size in bytes:", file_size)
```

## os.stat()
The `os.stat()` method returns the file size in bytes as a tuple.

```python
import os

file_stats = os.stat("example.txt")
print("File size in bytes:", file_stats.st_size)
```

## Pathlib
The `Pathlib` module provides a convenient way to check the file size.

```python
from pathlib import Path

file_size = Path("example.txt").stat().st_size
print("File size in bytes:", file_size)
```
