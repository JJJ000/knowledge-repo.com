---
title: What is the method to display only the main level directories in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Using `os.listdir()` with a comprehension to filter subdirectories `[d for d in os.listdir() if os.path.isdir(d)]`.
---

**Contents**

[TOC]

## Introduction

In Python, directories or folders can be listed using the `os` module. However, sometimes we might want to list only the top-level directories in a given folder. In this tutorial, we will explore some ways to achieve this.

## Using os.listdir() and os.path.isdir()

One way to list only top level directories is by using the `os.listdir()` function and checking if each item in the list is a directory or not using the `os.path.isdir()` function.

``` python
import os

# specify the path of the folder to be listed
path = '/path/to/folder'

# get the list of items in the folder
items = os.listdir(path)

# iterate through each item and check if it is a directory
for item in items:
    if os.path.isdir(os.path.join(path, item)):
        print(item)
```

In the above code, we first get the list of all items in the folder using `os.listdir()` function. Then we iterate through each item and check if it is a directory using `os.path.isdir()` function. If the item is a directory, we print its name.

## Using os.scandir() and DirEntry.is_dir()

Another way to achieve the same is by using the `os.scandir()` function and the `DirEntry.is_dir()` method.

``` python
import os

# specify the path of the folder to be listed
path = '/path/to/folder'

# get a generator of directory entries
entries = os.scandir(path)

# iterate through each entry and check if it is a directory
for entry in entries:
    if entry.is_dir():
        print(entry.name)
```

In the above code, we first get a generator of all directory entries in the folder using `os.scandir()` function. We then iterate through each entry and check if it is a directory using the `DirEntry.is_dir()` method. If the entry is a directory, we print its name.

## Using glob.glob()

Another way to list only top-level directories is by using the `glob.glob()` function.

``` python
import glob

# specify the path of the folder to be listed
path = '/path/to/folder'

# get a list of all directories in the folder
directories = glob.glob(path + '/*/')

# iterate through each directory and print its name
for directory in directories:
    print(directory.split('/')[-2])
```

In the above code, we use the `glob.glob()` function to get a list of all directories in the folder. We then iterate through each directory and print its name.

## Conclusion

In this tutorial, we have explored three ways to list only top-level directories in Python. The choice of method depends on personal preference and the specific use case.
