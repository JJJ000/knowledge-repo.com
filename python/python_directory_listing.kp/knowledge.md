---
title: How to list directories, subdirectories, and files in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `os.walk()` method in Python to list all directories, subdirectories, and files in a given directory path.
---

**Contents**

[TOC]

## Section 1: Introduction

Python provides several modules to work with the file system, and one of them is the `os` module. Using the `os` module, you can list all the directories, subdirectories, and files available in the specified directory path. This feature has a lot of practical applications, such as identifying the files present in a given directory and their respective subdirectories, filtering the results based on specific criteria, among others.


## Section 2: List directories and files in a directory

To list all the directories and files in a particular directory using Python, you can use the `os.listdir()` method. Let's see an example:


```python
import os

path = '/my_path/'
directories_and_files = os.listdir(path)

print(directories_and_files)
```


In this example, the `os.listdir()` method is used to get a list of all the directories and files in the `path` directory. This list is then printed on the screen.


## Section 3: List directories and files in subdirectories

To list all directories and files in the subdirectories, you can use the `os.walk()` function. The `os.walk()` function generates the file names in a directory tree by walking the tree either top-down or bottom-up. Let's see an example:


```python
import os

path = '/my_path'

for root, directories, files in os.walk(path):
    for filename in files:
        print(os.path.join(root, filename))
```


Here, the `os.walk()` function is used to traverse the directory tree rooted at the `path`. As it recursively traverses the directory tree, it returns the files in each directory along with their respective paths.


## Section 4: Filter files based on certain criteria

If you want to filter the files based on certain criteria like extension, filename, or size, you can use the `glob` module of Python. Let's see an example:


```python
import glob

path = '/my_path/*.txt'

for filename in glob.glob(path):
    print(filename)
```


Here, the `glob.glob()` function is used to find files whose name matches the specified pattern. In this case, all the `txt` files in the `my_path` directory are returned.
