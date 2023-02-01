---
title: What is the procedure for changing the active directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the os.chdir() function to set the current working directory in Python.
---

**Contents**

[TOC]

# Using os.chdir

The `os.chdir` function can be used to set the current working directory in Python. The syntax is as follows:

`os.chdir(path)`

Where `path` is the path of the directory you want to set as the current working directory.

# Using pathlib

The `pathlib` module can also be used to set the current working directory in Python. The syntax is as follows:

`Path.cwd(path)`

Where `path` is the path of the directory you want to set as the current working directory.

# Using shutil

The `shutil` module can also be used to set the current working directory in Python. The syntax is as follows:

`shutil.chdir(path)`

Where `path` is the path of the directory you want to set as the current working directory.

# Using os.getcwd

The `os.getcwd` function can be used to get the current working directory in Python. The syntax is as follows:

`os.getcwd()`

This will return the path of the current working directory.
