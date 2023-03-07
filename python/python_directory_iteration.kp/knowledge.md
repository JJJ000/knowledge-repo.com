---
title: Traversing directories using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can iterate through directories in Python using the os module and its various methods.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, iterating through directories involves the process of accessing and listing the contents of a directory/folder in a systematic way. The aim may be to get the names of all files/folders, their sizes, permission, creation/modification date, and so on. 

Section 2: Using os module for directory iteration
One popular way to iterate through directories in Python is to use the built-in module called os. This module provides useful functions and methods that can help to list files and directories, check permissions, and perform other file-related operations. To use the os module for directory iteration, follow these steps:
1. Import the os module at the beginning of the script using: 

`import os`

2. Use the `os.listdir()` method to get a list of all files and directories present in a given path. For example, to get a list of all files/folders inside the Documents folder, use the following code: 

```
path = "/home/user/Documents"
files = os.listdir(path)
print(files)
```
This will print the list of all files and sub-directories inside the Documents folder.

3. To iterate through the contents of a directory, use a for loop with the `os.listdir()` method. An example of iterating over all files inside the Documents folder is shown below:

```
path = "/home/user/Documents"
for file in os.listdir(path):
    print(file)
```

Section 3: Using pathlib module for directory iteration
Another useful way to iterate through directories is to use the pathlib module. This module provides an object-oriented interface and can be more intuitive to work with than using os. To use pathlib for directory iteration, follow these steps:
1. Import the pathlib module at the beginning of the script using:

`from pathlib import Path`

2. Create a Path object providing the path to the directory you want to iterate through. For example:

```
path = Path("/home/user/Documents")
```

3. Use the `path.iterdir()` method to iterate over all files and directories inside the provided path. An example of iterating over all files inside the Documents folder is shown below:

```
path = Path("/home/user/Documents")
for file in path.iterdir():
    print(file.name)
```

4. You can also filter the results by using the `.is_dir()` and `.is_file()` methods of the Path object. For example, to list only directories inside the Documents folder:

```
path = Path("/home/user/Documents")
for dir in path.iterdir():
    if dir.is_dir():
        print(dir.name)
```

Section 4: Conclusion
Iterating through directories is an essential operation when working with files in Python. The os and pathlib modules are both excellent ways to achieve this goal. The os module provides a functional approach to working with directoriies, while pathlib provides a more object-oriented way to access and manipulate file paths. It is worth considering the pros and cons of each module to determine which one is the best for your use case.
