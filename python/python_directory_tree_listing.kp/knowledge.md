---
title: Listing the directory tree structure in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The os.walk() function can be used to generate a directory tree listing in Python.
---

**Contents**

[TOC]

# Section 1: Creating Directory Tree

Python provides a variety of modules for creating directory trees. The most commonly used modules are os, shutil, and pathlib. 

## os Module
The os module provides a number of functions for interacting with the operating system. The os.makedirs() function can be used to create a directory tree. It takes a single argument which is the path of the directory tree to be created. The following example creates a directory tree at the path ‘/tmp/test/dir1/dir2’:

```python
import os

os.makedirs('/tmp/test/dir1/dir2')
```

## shutil Module
The shutil module provides a number of functions for manipulating files and directories. The shutil.copytree() function can be used to create a directory tree. It takes two arguments: the path of the source directory tree and the path of the destination directory tree. The following example creates a directory tree at the path ‘/tmp/test/dir1/dir2’ from the source directory tree at the path ‘/home/user/source’:

```python
import shutil

shutil.copytree('/home/user/source', '/tmp/test/dir1/dir2')
```

## pathlib Module
The pathlib module provides an object-oriented interface for interacting with the filesystem. The Path.mkDIR() method can be used to create a directory tree. It takes a single argument which is the path of the directory tree to be created. The following example creates a directory tree at the path ‘/tmp/test/dir1/dir2’:

```python
from pathlib import Path

Path('/tmp/test/dir1/dir2').mkdir(parents=True)
```

# Section 2: Listing Directory Tree

Python provides a variety of modules for listing directory trees. The most commonly used modules are os, shutil, and pathlib.

## os Module
The os module provides a number of functions for interacting with the operating system. The os.walk() function can be used to list a directory tree. It takes a single argument which is the path of the directory tree to be listed. The following example lists the directory tree at the path ‘/tmp/test/dir1/dir2’:

```python
import os

for root, dirs, files in os.walk('/tmp/test/dir1/dir2'):
    print(root, dirs, files)
```

## shutil Module
The shutil module provides a number of functions for manipulating files and directories. The shutil.copytree() function can be used to list a directory tree. It takes two arguments: the path of the source directory tree and the path of the destination directory tree. The following example lists the directory tree at the path ‘/tmp/test/dir1/dir2’ from the source directory tree at the path ‘/home/user/source’:

```python
import shutil

for root, dirs, files in shutil.copytree('/home/user/source', '/tmp/test/dir1/dir2'):
    print(root, dirs, files)
```

## pathlib Module
The pathlib module provides an object-oriented interface for interacting with the filesystem. The Path.iterdir() method can be used to list a directory tree. It takes a single argument which is the path of the directory tree to be listed. The following example lists the directory tree at the path ‘/tmp/test/dir1/dir2’:

```python
from pathlib import Path

for path in Path('/tmp/test/dir1/dir2').iterdir():
    print(path)
```
