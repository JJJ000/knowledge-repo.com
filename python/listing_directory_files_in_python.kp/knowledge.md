---
title: How to list all of the files in a directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To list all files of a directory in Python, use the `os.listdir()` function.
---

**Contents**

[TOC]

### Using os.listdir()

The `os.listdir()` method can be used to list all files in a directory.

Syntax:
```python
os.listdir(path)
```

Parameters:
- path: This is the path of the directory from which you want to list all the files. 

Return Value:
This method returns a list of files in the specified directory.

Example:
```python
import os

# List all files in a directory
files = os.listdir("/mydir")

for file in files:
    print(file)
```

### Using glob.glob()

The `glob.glob()` method can be used to list all files in a directory.

Syntax:
```python
glob.glob(pathname)
```

Parameters:
- pathname: This is the path of the directory from which you want to list all the files. 

Return Value:
This method returns a list of files in the specified directory.

Example:
```python
import glob

# List all files in a directory
files = glob.glob("/mydir/*")

for file in files:
    print(file)
```
