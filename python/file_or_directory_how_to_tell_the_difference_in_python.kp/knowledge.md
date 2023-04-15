---
title: What are the ways to distinguish a regular file from a directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the isfile() and isdir() methods from the os.path module in Python to identify whether a file is normal or directory respectively.
---

**Contents**

[TOC]

## 1. Use os.path module

The `os.path` module provides a function called `isfile()` which can be used to check whether a file exists and is a regular file (not directory, symlink, etc.).

``` python
import os

path = '/path/to/file_or_directory'

if os.path.isfile(path):
    print("File exists and is a normal file.")
else:
    print("Path does not exist or is not a normal file.")
```

## 2. Use os module

You can also use the `os` module to check whether a file exists and is a regular file using the `stat()` method.

``` python
import os

path = '/path/to/file_or_directory'

try:
    stat = os.stat(path)
    if stat.st_mode & 0o170000 == 0o100000:
        print("File exists and is a normal file.")
    else:
        print("Path does not exist or is not a normal file.")
except OSError:
    print("Path does not exist or is not a normal file.")
```

## 3. Use pathlib.Path module

The `pathlib.Path` module provides a method to check whether a path is a file using the `is_file()` method.

``` python
from pathlib import Path

path = Path('/path/to/file_or_directory')

if path.is_file():
    print("File exists and is a normal file.")
else:
    print("Path does not exist or is not a normal file.")
```

## 4. Use try-except block

If you want a more concise code, you can use a try-except block to check whether a path is a file or directory.

``` python
import os

path = '/path/to/file_or_directory'

try:
    is_file = os.path.isfile(path)
except OSError:
    is_file = False

if is_file:
    print("File exists and is a normal file.")
else:
    print("Path does not exist or is not a normal file.")
```
