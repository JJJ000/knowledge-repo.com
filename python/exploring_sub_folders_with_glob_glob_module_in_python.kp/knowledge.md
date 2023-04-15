---
title: What is the method to utilize glob.glob module for searching sub-folders?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The asterisk (*) can be used to search sub-folders along with the current directory while using the glob.glob module in Python.
---

**Contents**

[TOC]

Section 1: Understanding glob.glob module
The glob.glob module is used to retrieve files or directories from a specified path. It returns a list of file or directory paths that match the specified pattern.

Section 2: Searching sub-folders using glob.glob module
To search sub-folders using glob.glob module, you can use the ** wildcard. For example, if you want to search for all the .txt files in a directory and its sub-directories, you can use the following code:

``` python
import glob

file_list = glob.glob('/path/to/directory/**/*.txt', recursive=True)
```

This will search for all the .txt files in the specified directory and its sub-directories.

Section 3: Recursive parameter in glob.glob module
The recursive parameter in the glob.glob module is used to search for files or directories recursively. By setting the recursive parameter to True, the glob.glob module will search for files or directories in all sub-directories of the specified directory.

Section 4: Using other wildcards
Apart from the ** wildcard, you can also use other wildcards such as *, ? and [ ] to search for files or directories with specific patterns. For example, if you want to search for all the files that start with 'file' and end with '.txt', you can use the following code:

``` python
import glob

file_list = glob.glob('/path/to/directory/file*.txt')
```

This will search for all the files that start with 'file' and end with '.txt'.
