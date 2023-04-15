---
title: What is the procedure for determining if a directory exists in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the os.path.exists() method to check if a directory exists in Python.
---

**Contents**

[TOC]

1. Using `os.path.exists`
---------------------------------
The `os.path.exists` method can be used to check whether a directory exists. It takes a single argument, the path of the directory, and returns `True` if it exists, and `False` otherwise.

Example:
```python
import os

if os.path.exists('/path/to/dir'):
    print('Directory exists')
else:
    print('Directory does not exist')
```

2. Using `os.path.isdir`
---------------------------------
The `os.path.isdir` method can also be used to check whether a directory exists. It takes a single argument, the path of the directory, and returns `True` if it exists, and `False` otherwise.

Example:
```python
import os

if os.path.isdir('/path/to/dir'):
    print('Directory exists')
else:
    print('Directory does not exist')
```

3. Using `os.listdir`
---------------------------------
The `os.listdir` method can be used to check whether a directory exists. It takes a single argument, the path of the directory, and returns a list of the files and directories in the directory if it exists, and an empty list otherwise.

Example:
```python
import os

if os.listdir('/path/to/dir'):
    print('Directory exists')
else:
    print('Directory does not exist')
```

4. Using `os.stat`
---------------------------------
The `os.stat` method can also be used to check whether a directory exists. It takes a single argument, the path of the directory, and returns information about the directory if it exists, and an error otherwise.

Example:
```python
import os

try:
    os.stat('/path/to/dir')
    print('Directory exists')
except OSError:
    print('Directory does not exist')
```
