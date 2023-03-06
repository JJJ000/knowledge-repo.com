---
title: What is the method to identify the version of Python being used in jupyter notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Run the command `!python --version` in a notebook cell to know which Python version is running.
---

**Contents**

[TOC]

# Introduction

Jupyter notebook is an interactive coding environment that supports multiple programming languages. One of the most popular languages used with Jupyter notebook is Python. Oftentimes, if multiple versions of Python are installed on a system, it can be confusing to determine which Python version is being used within a Jupyter notebook.


# Check the Python version within Jupyter notebook

One way to check the Python version that Jupyter notebook is using is to run a simple Python script that prints out the version information. This can be done by running the following code snippet in a code cell within the notebook:

```
import sys
print(sys.version)
```

This will print out the full version information for the Python interpreter that Jupyter notebook is using. 


# Check the kernel version within Jupyter notebook

Another way to determine which version of Python is being used in Jupyter notebook is to check the kernel information. Jupyter notebook runs on a kernel, which is responsible for executing and interpreting the code within the notebook. Each kernel is associated with a specific programming language and version.

To check the kernel version within Jupyter notebook, you can click on the "Kernel" menu option in the top navigation bar and then select "Restart & Run All". This will restart the kernel and run all cells within the notebook. During the restart process, you will see a banner message that displays the kernel information, including the programming language and version.

Additionally, you can check the kernel information by running the following command in a code cell within the notebook:

```
import platform
print(platform.python_version())
```

This will print out the specific version of Python that the kernel is running. 


# Check the environment within Jupyter notebook

In some cases, multiple versions of Python may be installed within different environments on the same system. To check which environment Jupyter notebook is using, you can run the following code snippet in a code cell within the notebook:

```
import os
print(os.environ['PATH'])
```

This will print out the current environment variable PATH, which includes a list of directories where Python looks for executable files. By inspecting the directory paths listed in the output, you can determine which environment Jupyter notebook is using.
