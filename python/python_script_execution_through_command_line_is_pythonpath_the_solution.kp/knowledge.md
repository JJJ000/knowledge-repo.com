---
title: Is there a way to execute a Python script in the command line without changing the directory to where it is stored? is it possible to use the pythonpath for this?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Add the directory containing the Python script to the PATH environment variable.
---

**Contents**

[TOC]

## Introduction

Python is a popular programming language that is used for various applications today. One of the major advantages of using Python is the ease with which it can be integrated with other systems. When working with Python scripts on the command line, it is often necessary to use the scripts without CDs to their respective directories. This article explores some of the ways in which this can be done.

## Use the PYTHONPATH environment variable

One way of using a Python script without CD-ing to its directory is by setting the PYTHONPATH environment variable. The PYTHONPATH environment variable is a list of directories that Python should add to the search path. By adding the directory containing the script to the PYTHONPATH, Python will be able to find and execute the script without requiring the user to change the working directory. Here is how to set the PYTHONPATH variable:

```bash
export PYTHONPATH=/path/to/script/directory:$PYTHONPATH
```

## Use a symbolic link

Another way of using a Python script without CD-ing to its directory is by creating a symbolic link to the script in a directory that is already in the search path. This way, the user can execute the script from anywhere in the file system. Here is how to create a symbolic link:

```bash
ln -s /path/to/script /usr/local/bin
```

## Use the PATH environment variable

The PATH environment variable is a list of directories that the operating system searches when the user runs a command. By adding the directory containing the script to the PATH, the user can execute the script without requiring the user to change the working directory. Here is how to add the directory to the PATH variable:

```bash
export PATH=/path/to/script/directory:$PATH
```

## Conclusion

In this article, we have explored some of the ways in which a Python script can be executed without requiring the user to CD to its directory. These methods are useful in scenarios where the user needs to execute Python scripts quickly from different locations in the file system. By using the PATH, PYTHONPATH, and symbolic links, the user can execute Python scripts easily and efficiently.
