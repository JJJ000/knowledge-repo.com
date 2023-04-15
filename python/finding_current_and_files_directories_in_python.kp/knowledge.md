---
title: Determine the present directory and the directory of the file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The current directory can be found using the `os.getcwd()` function and the file's directory can be found using the `os.path.dirname()` function.
---

**Contents**

[TOC]

### Current Directory

The current directory can be retrieved using the `os.getcwd()` command.

```python
import os

current_dir = os.getcwd()
print(current_dir)
```

### File's Directory

The directory of a file can be retrieved using the `os.path.dirname()` command.

```python
import os

file_dir = os.path.dirname('/path/to/file.txt')
print(file_dir)
```
