---
title: The aim of the python3 project is to eliminate __pycache__ directories and .pyc files
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use the command `find . -name `*.pyc` -delete; find . -name `\_\_pycache\_\_` -delete` to remove both \_\_pycache\_\_ folders and .pyc files.
---

**Contents**

[TOC]

## Introduction

Python creates `__pycache__` folders to store compiled bytecode files (`.pyc` files) for performance optimization. These files are recompiled every time you make changes to the source code. Over time, these files and folders can accumulate and take up unnecessary disk space. Therefore, it's a good practice to remove them periodically to free up space.

In this article, we'll explore different ways to remove `__pycache__` folders and `.pyc` files from a Python project.

## Method 1: Delete manually

The easiest and straightforward way to remove `__pycache__` folders and `.pyc` files is to delete them manually using your computer's file explorer. Go to the root directory of your project and look for `__pycache__` folders and `.pyc` files. Delete them one by one or select multiple folders or files and delete them together.

This method may be time-consuming if you have many `__pycache__` folders or `.pyc` files to delete. Moreover, it's not efficient if you want to automate the process or delete them regularly.

## Method 2: Using the terminal

Another way to delete `__pycache__` folders and `.pyc` files from a Python project is to use the terminal or command prompt. Open the terminal or command prompt and navigate to the root directory of your Python project. Then, type the following commands to remove `__pycache__` folders and `.pyc` files, respectively.

```sh
rm -rf __pycache__
```

```sh
find . -name "*.pyc" -delete
```

The first command removes all `__pycache__` folders recursively in the current directory and its subdirectories. The second command finds all `.pyc` files in the current directory and its subdirectories and deletes them.

You can combine both commands into one like this:

```sh
rm -rf __pycache__ && find . -name "*.pyc" -delete
```

This command first removes all `__pycache__` folders and then deletes all `.pyc` files.

## Method 3: Using Python script

If you want to automate the process of removing `__pycache__` folders and `.pyc` files from a Python project, you can use a Python script. Here's an example script that does the same thing as the previous method.

```python
import os

def remove_pycache():
    for root, dirs, files in os.walk("."):
        for dir in dirs:
            if dir == "__pycache__":
                path = os.path.join(root, dir)
                print(f"Removing {path} ...")
                os.removedirs(path)

def remove_pyc():
    for root, dirs, files in os.walk("."):
        for file in files:
            if file.endswith(".pyc"):
                path = os.path.join(root, file)
                print(f"Removing {path} ...")
                os.remove(path)

if __name__ == "__main__":
    remove_pycache()
    remove_pyc()
```

This script recursively searches for `__pycache__` folders and `.pyc` files in the current directory and its subdirectories and removes them. You can save this script in your project directory and run it whenever you want to remove `__pycache__` folders and `.pyc` files.

## Conclusion

Removing `__pycache__` folders and `.pyc` files is essential to maintain a clean and organized Python project. You can do it manually, using the terminal, or a Python script according to your preference. The choice depends on the number of files and folders you want to remove and how frequently you want to do it.
