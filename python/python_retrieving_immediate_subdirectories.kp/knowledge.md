---
title: What is the way to obtain all the immediate subdirectories using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the os.listdir() method to get a list of all items (files and directories) in the current directory, then filter out the directories using os.path.isdir().
---

**Contents**

[TOC]

## 1. Importing required modules

The first section of the answer is to import the required Python modules to access the file system.

```python
import os
```

We use the `os` module to access the file system and retrieve the list of directories.


## 2. Retrieving subdirectories

The second section of the answer is to use the `os` module to retrieve the immediate subdirectories of a given directory.

```python
def get_immediate_subdirectories(dir_path):
    """
    Returns a list of immediate subdirectories of the given directory path
    """
    return [f.path for f in os.scandir(dir_path) if f.is_dir()]
```

The `get_immediate_subdirectories` function takes a directory path as an argument and returns a list of immediate subdirectories of the given directory path.

We use the `os.scandir` function to retrieve the list of files and directories in the given directory path. We filter only the directories using the `f.is_dir()` method, and return their path using the `f.path` property.


## 3. Using the function

The third section of the answer is an example of how to use the `get_immediate_subdirectories` function.

```python
dir_path = '/path/to/directory'

subdirectories = get_immediate_subdirectories(dir_path)

print(subdirectories)
```

We define the `dir_path` variable as the path to the directory for which we want to retrieve the immediate subdirectories. We call the `get_immediate_subdirectories` function with this argument and assign the result to the `subdirectories` variable. We then print the list of subdirectories using the `print` function.


## 4. Full code

The final section of the answer is the full code that combines the previous sections.

```python
import os

def get_immediate_subdirectories(dir_path):
    """
    Returns a list of immediate subdirectories of the given directory path
    """
    return [f.path for f in os.scandir(dir_path) if f.is_dir()]

dir_path = '/path/to/directory'

subdirectories = get_immediate_subdirectories(dir_path)

print(subdirectories)
```

This code can be run to retrieve the list of immediate subdirectories of the directory at the specified path.
