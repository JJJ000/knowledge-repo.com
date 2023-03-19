---
title: Create a singular executable file using py2exe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Py2exe is a Python module that can convert Python scripts into standalone executable files, but it can`t generate a single executable file.
---

**Contents**

[TOC]

## Introduction

In Python, it is possible to compile a script into a standalone executable file using the py2exe module. This can be useful for distributing Python programs to users who do not have Python installed on their machines, or for packaging an application into a single executable file for ease of distribution.

## Installing py2exe

Before using py2exe, you must first install it. The easiest way to do this is to use pip, the Python package manager. To install py2exe with pip, open a command prompt and type:

```
pip install py2exe
```

## Using py2exe

Once py2exe is installed, you can use it to compile your Python script into a standalone executable file. To do this, create a setup.py file in the same directory as your script. The setup.py file should contain information about the script, such as its name, version, and author, as well as instructions for py2exe on how to package it.

Here is an example of a setup.py file:

```
from distutils.core import setup
import py2exe
setup(console=['my_script.py'])
```

In this example, my_script.py is the name of the script that you want to package into an executable file. To create the executable file, run the command:

```
python setup.py py2exe
```

This will generate an executable file in the dist directory of your project.

## Conclusion

Using py2exe, you can easily package Python scripts into standalone executable files. This can be helpful for distributing Python applications to users who do not have Python installed on their machines, or for packaging an application into a single executable file for ease of distribution.
