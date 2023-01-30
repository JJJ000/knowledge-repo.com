---
title: What is the process for obtaining file creation and modification date/times?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can get file creation and modification date/times in Python using the os.stat() method.
---

**Contents**

[TOC]

## Using os.stat

The `os.stat` function can be used to retrieve information about the given file. This includes the file creation and modification date/times.

Syntax: `os.stat(path)`

Example:

```python
import os

# Get file stats
stats = os.stat('myfile.txt')

# Get file creation and modification date/times
creation_time = stats.st_ctime
modification_time = stats.st_mtime
```

## Using os.path.getctime and os.path.getmtime

The `os.path.getctime` and `os.path.getmtime` functions can also be used to retrieve the file creation and modification date/times, respectively.

Syntax: 

`os.path.getctime(path)`

`os.path.getmtime(path)`

Example:

```python
import os

# Get file creation and modification date/times
creation_time = os.path.getctime('myfile.txt')
modification_time = os.path.getmtime('myfile.txt')
```
