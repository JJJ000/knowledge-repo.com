---
title: How to find the size of a file in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The size of a file in Python can be retrieved using the os.stat() function.
---

**Contents**

[TOC]

### Using os.path

The `os.path` module provides functions to get the size of a file in Python. The `os.path.getsize()` method returns the size of a file in bytes.

```python
import os

file_path = 'path/to/file.txt'
file_size = os.path.getsize(file_path)
print('The size of the file is', file_size, 'bytes')
```

### Using Pathlib

The `Pathlib` module provides an object-oriented way to access files and directories in Python. The `Path.stat()` method returns information about a file or directory, including its size in bytes.

```python
from pathlib import Path

file_path = Path('path/to/file.txt')
file_size = file_path.stat().st_size
print('The size of the file is', file_size, 'bytes')
```

### Using shutil

The `shutil` module provides a `shutil.disk_usage()` method which returns the size of a file or directory in bytes.

```python
import shutil

file_path = 'path/to/file.txt'
file_size = shutil.disk_usage(file_path).used
print('The size of the file is', file_size, 'bytes')
```
