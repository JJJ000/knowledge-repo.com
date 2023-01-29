---
title: What is the procedure for relocating a file using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the shutil.move() function to move a file in Python.
---

**Contents**

[TOC]

# Using the os Module

The `os` module provides functions for interacting with the operating system. To move a file, you can use the `os.rename()` function.

## Syntax

The syntax for `os.rename()` is as follows:

```python
os.rename(src, dst)
```

Where `src` is the current path of the file and `dst` is the new path of the file.

## Example

The following example moves a file from the current directory to a new directory:

```python
import os

src = 'old_file.txt'
dst = 'new_directory/new_file.txt'

os.rename(src, dst)
```

# Using the shutil Module

The `shutil` module provides functions for high-level file operations. To move a file, you can use the `shutil.move()` function.

## Syntax

The syntax for `shutil.move()` is as follows:

```python
shutil.move(src, dst)
```

Where `src` is the current path of the file and `dst` is the new path of the file.

## Example

The following example moves a file from the current directory to a new directory:

```python
import shutil

src = 'old_file.txt'
dst = 'new_directory/new_file.txt'

shutil.move(src, dst)
```
