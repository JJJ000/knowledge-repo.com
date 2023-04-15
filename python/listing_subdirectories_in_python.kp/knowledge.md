---
title: Retrieving a collection of all subfolders in the present folder
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: os.listdir(`.`) can be used to get a list of all subdirectories in the current directory in Python.
---

**Contents**

[TOC]

# Section 1: Using os.listdir()
The `os.listdir()` method can be used to get a list of all the subdirectories in the current directory.

# Section 2: Syntax
The syntax for using `os.listdir()` is as follows:

```python
import os

subdirectories = [f for f in os.listdir('.') if os.path.isdir(f)]
```

# Section 3: Explanation
The `os.listdir()` method will return a list of all the files and directories in the current directory. The `os.path.isdir()` method is then used to filter out all the files and only return the subdirectories.

# Section 4: Output
The output of the `os.listdir()` method will be a list of all the subdirectories in the current directory.
