---
title: Check if a Python program is executable
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the os.path.isfile() function to test if an executable exists in Python.
---

**Contents**

[TOC]

# Section 1: Using os.path

The os.path module provides a number of useful functions related to file and directory paths. It can be used to check if a file or directory exists using the `os.path.exists()` function.

```python
import os

file_name = 'my_file.txt'

if os.path.exists(file_name):
    print('File exists')
else:
    print('File does not exist')
```

# Section 2: Using Pathlib

The Pathlib module is a more modern and object-oriented way of dealing with files and directories. It provides a `Path.exists()` method which can be used to check if a file or directory exists.

```python
from pathlib import Path

file_name = Path('my_file.txt')

if file_name.exists():
    print('File exists')
else:
    print('File does not exist')
```

# Section 3: Using os.access

The os.access() function can be used to check if a file or directory exists and if the current user has permission to access it.

```python
import os

file_name = 'my_file.txt'

if os.access(file_name, os.F_OK):
    print('File exists')
else:
    print('File does not exist')
```

# Section 4: Using shutil

The shutil module provides a number of high-level file and directory operations. It can be used to check if a file or directory exists using the `shutil.which()` function.

```python
import shutil

file_name = 'my_file.txt'

if shutil.which(file_name):
    print('File exists')
else:
    print('File does not exist')
```
