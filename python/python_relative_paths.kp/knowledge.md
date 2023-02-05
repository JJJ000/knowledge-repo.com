---
title: Paths in Python that are relative to a file or directory's location
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Relative paths in Python refer to file paths relative to the current working directory.
---

**Contents**

[TOC]

# 1. What is a Relative Path?
A relative path is a path that is relative to the current working directory. It is a way to specify a file or directory on a computer without having to provide the full path from the root directory.

# 2. How to Use Relative Paths in Python
In Python, relative paths can be used with the `os.path.join()` method. This method takes two arguments, a directory path and a file path, and combines them into a single path relative to the current working directory.

# 3. Examples of Relative Paths
For example, if the current working directory is `/home/user/Documents` and you want to access a file located in `/home/user/Downloads/file.txt`, then the relative path would be `os.path.join('Downloads', 'file.txt')`.

# 4. Benefits of Using Relative Paths
Using relative paths helps to ensure that your code will work on different systems and directories. It also makes your code more portable and easier to read.
