---
title: Creating nested directories in Python using the 'mkdir -p' command
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: The `os.mkdir` function can be used to create a new directory in Python.
---

**Contents**

[TOC]

### os.makedirs()
The `os.makedirs()` function in Python is used to create a directory and all intermediate directories if they do not exist. This function takes in the path of the directory to be created as an argument and returns `None` upon successful creation.

### Syntax
The syntax for `os.makedirs()` is as follows:
```
os.makedirs(path, mode=0o777, exist_ok=False)
```

### Parameters
* **path**: This parameter is required and is the path of the directory to be created.
* **mode**: This parameter is optional and is used to set the mode of the directory. The default value is 0o777.
* **exist_ok**: This parameter is optional and is used to specify whether to raise an exception if the directory already exists. The default value is False.

### Examples
Here are some examples of how to use `os.makedirs()`:
```
# Create a directory
os.makedirs('/my/new/directory')

# Create a directory with a specific mode
os.makedirs('/my/new/directory', mode=0o755)

# Create a directory if it does not exist
os.makedirs('/my/new/directory', exist_ok=True)
```
