---
title: What is the right way to open a file in the present script's directory with reliability?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the os module to get the absolute path of the currently running script and then use the os.path.join method to access the desired file in the same directory.
---

**Contents**

[TOC]

# Introduction

When writing Python scripts, it's common to want to read or write files that are located in the same directory as the script itself.
In this tutorial, we'll explore some approaches to reliably open a file in the same directory as the currently running Python script.

# 1. Using the `os` module to get the directory path

The `os` module provides a cross-platform way to interact with the filesystem. We can use it to get the directory path of the currently running script using the `os.path` and `os.getcwd()` functions.

``` python
import os

# Get the directory path of the currently running script
dir_path = os.path.dirname(os.path.realpath(__file__))
```

In this code snippet, `__file__` is a special variable that contains the path of the currently running script. `os.path.realpath()` returns the canonical path of the script, resolving any symbolic links or relative paths, and `os.path.dirname()` extracts the directory name from the path.

With `dir_path` set, we can use it to reference files in the same directory as the script. For example, to open a file named `data.txt`, we could use:

``` python
data_file_path = os.path.join(dir_path, 'data.txt')
with open(data_file_path, 'r') as f:
    # Do something with the file
```

Note that we used `os.path.join()` to concatenate the directory path and the file name in a platform-independent way.

# 2. Using `importlib.resources` to access package data

If your script is in a Python package, you can use the `importlib.resources` module (available from Python 3.7 onwards) to access data files in the package. 

Assuming your package has a data file named `data.txt` located in the same directory as the script, you can use:

``` python
import importlib.resources

data = importlib.resources.read_text(__package__, 'data.txt')
# Do something with the contents of `data`
```

Note that `__package__` is a special variable that contains the name of the current package. `read_text()` returns the content of the file as a string.

# 3. Using `pkg_resources` to access package data

If you're using an older version of Python or don't want to use `importlib`, you can use the `pkg_resources` module from the `setuptools` package to access package data.

Assuming your package has a data file named `data.txt` located in the same directory as the script, you can use:

``` python
import pkg_resources

data = pkg_resources.resource_string(__name__, 'data.txt')
# Do something with the contents of `data`
```

Note that `__name__` is a special variable that contains the name of the current module. `resource_string()` returns the content of the file as a bytes object.

# Conclusion

In this tutorial, we explored three approaches to reliably open a file in the same directory as the currently running Python script. By using the `os` module, `importlib.resources`, or `pkg_resources`, we can access files in the same directory regardless of the current working directory or the location of the script on the filesystem.
