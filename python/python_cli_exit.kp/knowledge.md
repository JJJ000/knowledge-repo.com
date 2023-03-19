---
title: Leaving the Python command line
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To exit from Python Command Line, type `exit()` or press `Ctrl + Z` followed by `enter` on Windows or `Ctrl + D` on Unix/Linux.
---

**Contents**

[TOC]

Sections:

1. Exiting on interactive mode
2. Exiting on script or non-interactive mode

## Exiting on interactive mode
Exiting from python Command Line or interactive mode is very simple. Pythons provides a convenient command, `exit()`, which terminates the interactive mode. To exit from interactive mode, follow the steps mentioned below:
1. Open the terminal or command prompt and type `python` to enter into the Python Interpreter or Interactive mode.
2. Now if you run multiple commands or execute the script, and you are done with it, then you need to type `exit()` and hit enter key. 

```python
$ python
Python 3.9.7 (default, Sep 16 2021, 08:50:36)
[Clang 12.0.5 (clang-1205.0.22.11)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> print('Hello World')
Hello World
>>> exit()
$
```

In the above example, we execute the `print` command, followed the `exit()` command, and it returned back to the command line prompt.

## Exiting on script or non-interactive mode
Python is a very powerful programming language and allows us to create test scripts, code snippets, or model development codes. We can run these codes in non-interactive or non-interactive mode within the shell. If we want to exit from a script or non-interactive mode, we can use the `sys` module to stop the program's execution. Follow the steps mentioned below to exit from the Python script:
1. Open any text editor and write the following code:

```python
import sys
# Your Additional Code here
sys.exit()
```

2. Replace "Your Additional Code here" with your actual code which can be anything, a function, or an import statement, etc.
3. Once it meets the exit() command, the program execution will stop without any error.

```python
import sys

print('Hello World')

sys.exit()

print('After Exit World')
```
In the above example, we executed print command, followed by `sys.exit()` command, which will terminate the execution, and the `print` statement won't execute.
