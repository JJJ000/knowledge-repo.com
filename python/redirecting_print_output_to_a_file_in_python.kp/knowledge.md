---
title: What is the method for directing the output of 'print' to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `>` operator and specify the file name to redirect the output of `print` to a file in Python.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides various ways to redirect output from the console/terminal to a file. The standard way to redirect the output of a print statement is by using the '>' character followed by the filename.

Section 2: Simple redirection using '>'
The simplest way to redirect output to a file is as follows:
```python
    with open('output.txt', 'w') as f:
        print('Hello, World!', file=f)
```
Upon execution, this script will create a file named 'output.txt' with the string 'Hello, World!' as its content.

Section 3: Redirecting multiple outputs to a file
If you have multiple print statements and want to redirect the output of all of them to a file, you can do it as follows:
```python
    with open('output.txt', 'w') as f:
        print('Hello, World!', file=f)
        print('This is a test!', file=f)
```
This will create a file named 'output.txt' and write both 'Hello, World!' and 'This is a test!' to the file.

Section 4: Appending to a file
If you want to append the output of print statements to a file instead of overwriting it, you can do this:
```python
    with open('output.txt', 'a') as f:
        print('Hello, World!', file=f)
        print('This is a test!', file=f)
```
This will create a file named 'output.txt' if it does not exist, and write both the 'Hello, World!' and 'This is a test!' strings to the file. If the file already exists, the new outputs will be appended to the end of the file.
