---
title: Using Python to remove all files from a directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can use the `os` module`s `listdir` and `remove` functions to delete all files in a directory.
---

**Contents**

[TOC]

# Introduction 

Python is a powerful programming language used for various purposes including file handling. In this tutorial, we will explore how to delete all files in a directory using Python.

# Importing Required Modules 

Before we proceed with the deletion of all files in a directory, we need to import some modules. These modules are:

- os module: used to perform operations on files and directories.

```python
import os
```

# Deleting all files in directory 

Now, we have important modules in our code, let's start with the process of deleting all files in a directory. We will use the `os` module to perform this operation. The `os` module provides a `listdir()` function that returns a list of all files and directories in the specified directory. 

```python
dir_path = 'path_to_directory'
for file in os.listdir(dir_path):
    file_path = os.path.join(dir_path, file)
    try:
        if os.path.isfile(file_path) or os.path.islink(file_path):
            os.unlink(file_path)
    except Exception as e:
        print('Failed to delete %s. Reason: %s' % (file_path, e))
```

In this code, we have specified the directory path in the `dir_path` variable. Then we loop through all files in that directory using the `listdir()` function. We use the `os.path.join()` function to get the absolute path of the file. Finally, we use the `os.unlink()` function to delete the file. 

# Conclusion 

In this tutorial, we learned how to delete all files in a directory using Python. We used the `os` module to perform this operation. With the help of the `os` module, we can perform various other operations on files and directories as per our requirements.
