---
title: Not including directories in os.walk
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To exclude directories in os.walk in Python, use the condition `if dirpath.endswith(`<directory\_name>`)` to skip over them.
---

**Contents**

[TOC]

Section 1: Introduction

`os.walk()` is a Python method used to traverse and search through a directory. It provides a convenient way to obtain a list of all the subdirectories in a directory tree. However, sometimes it is necessary to exclude certain directories while traversing the directory tree. This can be achieved by using the `topdown` and `dirs` arguments of the `os.walk()` method.

Section 2: Using the `topdown` argument

The `topdown` argument in `os.walk()` controls the order in which the directories are traversed. By default, the directories are traversed in a bottom-up manner, meaning that the subdirectories are processed before the parent directory. However, by setting the `topdown` argument to `False`, the traversal order is reversed, and the parent directory is processed before its subdirectories. 

This can be useful when excluding directories, as it allows us to remove unwanted directories before they are encountered while traversing the tree. Here is an example of how to exclude a directory called `dir1` when traversing a directory:

```
import os

dir_to_search = "/path/to/directory/to/search"

for root, dirs, files in os.walk(dir_to_search, topdown=True):
    if 'dir1' in dirs:
        dirs.remove('dir1')
        
    # Process remaining directories and files here
```

In this example, we check each subdirectory in `dirs` to see if it matches the name of the directory we want to exclude (`dir1`). If it does, we remove it from the list of directories.

Section 3: Using the `dirs` argument

The `dirs` argument of `os.walk()` can be used to specify a list of directories to exclude from the traversal. This allows us to exclude directories that match a certain pattern or have specific attributes. To use the `dirs` argument, we simply pass a list of directory names to be excluded as the value of the argument when calling `os.walk()`.

Here is an example of how to exclude directories that start with the letter "a" when traversing a directory:

```
import os

dir_to_search = "/path/to/directory/to/search"

exclude_dirs = ['a*', 'my_exclude_dir']

for root, dirs, files in os.walk(dir_to_search, topdown=False, dirs=exclude_dirs):
    # Process remaining directories and files here
```

In this example, we set the `topdown` argument to `False` to ensure that any excluded directories are removed before they are encountered. We pass a list of directory names to exclude, where `a*` matches any directory that starts with the letter "a", and `my_exclude_dir` matches a specific directory name.

Section 4: Conclusion

Excluding certain directories while traversing a directory tree can be achieved using the `topdown` and `dirs` arguments of the `os.walk()` method. In this way, we can selectively remove unwanted directories and process only the directories we want. This can make our code more efficient and reduce the errors that may arise from processing unwanted directories.
