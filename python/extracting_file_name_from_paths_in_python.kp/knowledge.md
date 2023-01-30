---
title: Obtain the file name from the directory path, regardless of the operating system or path format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The os.path.basename() function can be used to extract the file name from a path, regardless of the operating system or path format.
---

**Contents**

[TOC]

### Using os.path.basename

The `os.path.basename` method can be used to extract the file name from a path, regardless of the operating system or path format. This method takes a path as its argument and returns the last component of the path.

```python
import os

file_path = '/path/to/file.txt'
file_name = os.path.basename(file_path)

print(file_name) # prints 'file.txt'
```

### Using os.path.split

The `os.path.split` method can also be used to extract the file name from a path. This method takes a path as its argument and returns a tuple containing the head (everything up to the last component) and the tail (the last component) of the path. The tail of the path is the file name.

```python
import os

file_path = '/path/to/file.txt'
head, tail = os.path.split(file_path)

print(tail) # prints 'file.txt'
```

### Using os.path.splitext

The `os.path.splitext` method can be used to extract the file name and its extension from a path. This method takes a path as its argument and returns a tuple containing the root (everything up to the extension) and the extension of the path. The root of the path is the file name.

```python
import os

file_path = '/path/to/file.txt'
root, ext = os.path.splitext(file_path)

print(root) # prints 'file'
print(ext) # prints '.txt'
```

### Using Pathlib

The `Pathlib` module can also be used to extract the file name from a path. This module provides an object-oriented way of working with files and directories. The `name` attribute of a `Path` object contains the file name.

```python
from pathlib import Path

file_path = Path('/path/to/file.txt')
file_name = file_path.name

print(file_name) # prints 'file.txt'
```
