---
title: What is the process to create a .pyc file manually from a .py file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Run the command `python -m py\_compile filename.py` in your terminal or command prompt.
---

**Contents**

[TOC]

## Introduction

When we run a python script or import a module, Python interpreter compiles it into bytecode first and then execute it. The bytecode is stored in `.pyc` files (or `.pyo` files in Python 3), which are generated automatically and saved in the same directory as the corresponding module file. In this article, we will discuss how to manually generate `.pyc` files from `.py` files in Python.

## Creating a `.py` file

Before we can generate a `.pyc` file, we need to create a `.py` file first. It can be accomplished using any text editor or IDE of your choice. Here's an example python script that we'll use for this tutorial:

```python
# example.py
def greet(name):
    print(f"Hello, {name}!")

greet("World")
```

## Generating `.pyc` file using command-line interface

The most straightforward way to generate a `.pyc` file is to use the command-line interface. Here are the steps to generate a `.pyc` file using CLI:

1. Open up your terminal or command prompt
2. Navigate to the directory where your `.py` file resides using the `cd` command
3. Run the following command:

```
python -m py_compile example.py
```

This will generate a `example.pyc` file in the same directory as the `example.py` file.

## Generating `.pyc` file using `compileall` module

Another way to generate `.pyc` files is by using the `compileall` module in Python. The `compileall` module provides a command-line interface and a function that compiles all the `.py` files in a directory tree.

Here are the steps to generate a `.pyc` file using `compileall` module:

1. Open up your terminal or command prompt
2. Navigate to the directory where your `.py` file resides using the `cd` command
3. Run the following command:

```
python -m compileall .
```

The `.` specifies the current directory. This command will recursively compile all `.py` files and save the `.pyc` file in the same directory.

## Conclusion

In this article, we learned how to manually generate `.pyc` files from `.py` files in Python. We covered two methods - using the command-line interface and using the `compileall` module. While generating `.pyc` files manually is not necessary in most cases, it can be useful in certain situations, such as when we want to distribute pre-compiled modules or when we need to access the `.pyc` files for debugging purposes.
