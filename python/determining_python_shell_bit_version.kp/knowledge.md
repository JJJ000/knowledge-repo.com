---
title: What is the bit size of my Python shell?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can check the bit version of your Python shell by running the command `python -V` and looking at the output.
---

**Contents**

[TOC]

# Check Python Version

To determine if your Python shell is executing in 32bit or 64bit, you can first check the version of Python you are using.

To do this, open your Python shell and type in the following command:

`python --version`

This will return the version of Python you are running. If the version includes either the string `32bit` or `x86` then you are running a 32bit version of Python. If the version includes the string `64bit` or `x86_64` then you are running a 64bit version of Python.

# Check System Architecture

Another way to determine if your Python shell is executing in 32bit or 64bit is to check the system architecture of your computer.

To do this, open your command line and type in the following command:

`systeminfo`

This will return information about your system, including the system architecture. If the architecture is listed as `x86` then you are running a 32bit version of Python. If the architecture is listed as `x64` then you are running a 64bit version of Python.

# Check Python Executable

Finally, you can check the Python executable to determine if your Python shell is executing in 32bit or 64bit.

To do this, open your command line and type in the following command:

`where python`

This will return the location of the Python executable. If the path includes either the string `32bit` or `x86` then you are running a 32bit version of Python. If the path includes the string `64bit` or `x86_64` then you are running a 64bit version of Python.
