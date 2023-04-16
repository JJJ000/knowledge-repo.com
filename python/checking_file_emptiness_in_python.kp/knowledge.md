---
title: What is the method for determining if a file is empty?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To check if a file is empty or not in Python, use the os.stat() function to check the file size.
---

**Contents**

[TOC]

# Using os.stat

One way to check if a file is empty or not is to use the `os.stat` function. This function returns the status of a file as a `stat_result` object. This object contains information about the file such as its size, permissions, etc.

The `st_size` attribute of the `stat_result` object can be used to determine if a file is empty or not. If the size of the file is 0, then the file is empty.

```python
import os

file_name = 'file.txt'
if os.stat(file_name).st_size == 0:
    print('The file is empty')
else:
    print('The file is not empty')
```

# Using pathlib

Another way to check if a file is empty or not is to use the `Path` class from the `pathlib` library. This class provides a higher-level interface for working with files and directories.

The `stat` method of the `Path` class can be used to get the status of a file as a `stat_result` object. The `st_size` attribute of this object can be used to determine if a file is empty or not. If the size of the file is 0, then the file is empty.

```python
from pathlib import Path

file_name = 'file.txt'
if Path(file_name).stat().st_size == 0:
    print('The file is empty')
else:
    print('The file is not empty')
```

# Using the open function

The `open` function can also be used to check if a file is empty or not. The `open` function returns a file object which can be used to read the contents of the file.

The `read` method of the file object can be used to read the contents of the file. If the contents of the file are empty, then the file is empty.

```python
file_name = 'file.txt'
with open(file_name) as f:
    if f.read():
        print('The file is not empty')
    else:
        print('The file is empty')
```
