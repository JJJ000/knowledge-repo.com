---
title: Retrieve the relative path by comparing two absolute paths
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the `os.path.relpath()` function in Python to get the relative path from comparing two absolute paths.
---

**Contents**

[TOC]

## Section 1: Understanding the problem

To get the relative path from comparing two absolute paths in Python, we need to find the common path between them and remove it from each path. The resulting paths will be the relative paths.

For example, if we have the absolute paths `/home/user/documents/file.txt` and `/home/user/pictures/myphoto.jpg`, the common path is `/home/user`. The relative paths will be `documents/file.txt` and `pictures/myphoto.jpg`.

To implement this in Python, we will need to use some string manipulation and the `os` module.


## Section 2: Finding the common path

To find the common path between two absolute paths, we can split them into lists of directories and compare them. We will loop over the directories until we find the first one that is different, and join the common directories back into a path.

Here's some code that implements this:

```python
import os

def common_path(path1, path2):
    dirs1 = path1.split(os.sep)
    dirs2 = path2.split(os.sep)
    common_dirs = []
    for dir1, dir2 in zip(dirs1, dirs2):
        if dir1 == dir2:
            common_dirs.append(dir1)
        else:
            break
    return os.sep.join(common_dirs)
```

This function takes two absolute paths as arguments and returns the common path.


## Section 3: Getting the relative paths

Once we have the common path, we need to remove it from each absolute path to get the relative paths. We can do this using the `os.path.relpath` function, which calculates the relative path between two paths.

Here's how we can use it:

```python
def relative_paths(path1, path2):
    common = common_path(path1, path2)
    rel1 = os.path.relpath(path1, common)
    rel2 = os.path.relpath(path2, common)
    return rel1, rel2
```

This function takes two absolute paths as arguments and returns the relative paths as a tuple.


## Section 4: Testing the code

We can test our code with some example paths:

```python
path1 = "/home/user/documents/file.txt"
path2 = "/home/user/pictures/myphoto.jpg"
rel1, rel2 = relative_paths(path1, path2)
print(rel1)  # prints "documents/file.txt"
print(rel2)  # prints "pictures/myphoto.jpg"
```

This should print the relative paths between the two files correctly.
