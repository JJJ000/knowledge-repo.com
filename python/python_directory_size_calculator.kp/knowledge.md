---
title: How to use Python to determine the size of a directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the os module to recursively iterate through the directory and calculate the size of each file/folder, then sum them up to determine the total size of the directory.
---

**Contents**

[TOC]

## Intro
In this article, we will discuss how to calculate the size of a directory using Python. This can be useful for managing file storage and keeping track of how much space is being used.

## Using the os and os.path Modules
One approach to calculating directory size in Python is to utilize the `os` and `os.path` modules. The `os` module provides an interface to various operating system functions, while the `os.path` module provides functions to manipulate file and directory paths. Here's an example of using these modules:

``` python
import os

def get_dir_size(path='.'):
    total = 0
    with os.scandir(path) as it:
        for entry in it:
            if entry.is_file():
                total += entry.stat().st_size
            elif entry.is_dir():
                total += get_dir_size(entry.path)
    return total
```

This implementation recursively calculates the size of each file and directory in the given path, adding up the total size. The default path is the current directory, but you can pass in any path to calculate its size.

## Using the functools.lru_cache Decorator
Since calculating the directory size recursively can be an expensive operation, we can optimize our implementation using the `functools.lru_cache` decorator. This decorator caches the results of the function so that any subsequent calls with the same arguments don't need to recalculate the result. Here's the updated implementation:

``` python
import os
import functools

@functools.lru_cache(maxsize=128)
def get_dir_size(path='.'):
    total = 0
    with os.scandir(path) as it:
        for entry in it:
            if entry.is_file():
                total += entry.stat().st_size
            elif entry.is_dir():
                total += get_dir_size(entry.path)
    return total
```

With the decorator, the function is now much faster for repeated calls with the same arguments.

## Using the walking Method of os Module
An alternative implementation that doesn't require recursion is to use the `os.walk` function. This function returns a generator that recursively walks through a directory tree and yields information about each file and directory it encounters. Here's an example implementation:

``` python
import os

def get_dir_size(path='.'):
    total = 0
    with os.scandir(path) as it:
        for entry in it:
            if entry.is_file():
                total += entry.stat().st_size
            elif entry.is_dir():
                for root, dirs, files in os.walk(entry.path):
                    for file in files:
                        total += os.stat(os.path.join(root, file)).st_size
    return total
```

This implementation walks through each directory using `os.walk` and sums up the size of each file it encounters. It is less prone to stack overflow errors than the previous implementation, but it can be slightly slower for small directories.
