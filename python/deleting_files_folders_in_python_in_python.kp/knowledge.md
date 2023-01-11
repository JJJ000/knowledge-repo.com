---
title: What is the process for removing a file or folder using Python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: To delete a file or folder in Python, use the `os.remove()` or `os.rmdir()` functions.
---

**Contents**

[TOC]

### Using os.remove()

The `os.remove()` function can be used to delete a file in Python. It takes in the path of the file as an argument and deletes it from the system.

```python
import os

file_path = 'path/to/file.txt'
os.remove(file_path)
```

### Using os.rmdir()

The `os.rmdir()` function can be used to delete an empty directory in Python. It takes in the path of the directory as an argument and deletes it from the system.

```python
import os

dir_path = 'path/to/dir'
os.rmdir(dir_path)
```

### Using shutil.rmtree()

The `shutil.rmtree()` function can be used to delete a directory and all its contents in Python. It takes in the path of the directory as an argument and deletes it from the system.

```python
import shutil

dir_path = 'path/to/dir'
shutil.rmtree(dir_path)
```
