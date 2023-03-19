---
title: In python, perform recursive copying of directories or files
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the shutil module`s copytree() method to copy files or directories recursively in Python.
---

**Contents**

[TOC]

## Introduction

Python comes with various file management modules that help in operations such as copy, rename, delete, create and access files and directories. One of the common tasks is to copy files or directories recursively. In this article, we will look at how to do it in Python.

## Copying files using shutil

The `shutil` module in Python provides a simple way to copy files and directories.

To copy a file, `shutil.copy()` can be used. Here is an example:

```python
import shutil

src_file = "/path/to/source/file.txt"
dst_file = "/path/to/destination/file.txt"

shutil.copy(src_file, dst_file)
```

To copy a directory recursively, `shutil.copytree()` can be used. Here is an example:

```python
import shutil

src_dir = "/path/to/source/directory"
dst_dir = "/path/to/destination/directory"

shutil.copytree(src_dir, dst_dir)
```

## Copying files using os and shutil

Another way to copy files recursively is by using the `os` module to traverse the directory and `shutil` to copy the files.

Here is an example:

```python
import os
import shutil

src_dir = "/path/to/source/directory"
dst_dir = "/path/to/destination/directory"

for root, dirs, files in os.walk(src_dir):
    for file in files:
        src_file = os.path.join(root, file)
        dst_file = src_file.replace(src_dir, dst_dir, 1)
        dst_dirname = os.path.dirname(dst_file)
        if not os.path.exists(dst_dirname):
            os.makedirs(dst_dirname)
        shutil.copy2(src_file, dst_file)
```

In this example, `os.walk()` is used to traverse the directory, `os.path.join()` is used to create the full path of the source file and `os.path.exists()` is used to check if the destination directory exists before creating it.

## Copying files using distutils.dir_util

A third way to copy files recursively is by using the `distutils.dir_util` module.

Here is an example:

```python
import distutils.dir_util

src_dir = "/path/to/source/directory"
dst_dir = "/path/to/destination/directory"

distutils.dir_util.copy_tree(src_dir, dst_dir)
```

In this example, `distutils.dir_util.copy_tree()` is used to copy the source directory to the destination directory.

## Conclusion

In this article, we looked at three ways to copy files recursively in Python. The `shutil`, `os` and `distutils.dir_util` modules all provide simple ways to copy files and directories in Python.
