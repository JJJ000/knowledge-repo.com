---
title: How to run a Python program using a shell script
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To execute a Python program from within a shell script, use the command `python <filename.py>`.
---

**Contents**

[TOC]

Introduction
------------

Python is a popular interpreted language that is widely used for scripting and automation tasks. Shell scripting is another powerful tool for automating tasks in a Unix or Linux environment. In many cases, these two tools can complement each other when used together. For example, you might want to call a Python script from within a shell script. In this article, we will explore different ways to execute a Python program from a shell script.


Method 1: Call Python Interpreter Directly
------------------------------------------

The simplest way to execute a Python script from a shell script is to call the Python interpreter directly. To do this, you need to use the following command:

```sh
python path/to/your_script.py arg1 arg2 arg3
```

The `python` command is used to execute a Python script, and `path/to/your_script.py` is the path to your Python script. The `arg1 arg2 arg3` are the arguments that can be passed to your Python script. For example, let's say you have a Python script named `hello.py` that takes a name argument. You can call this script from a shell script like this:

```sh
#!/bin/sh
python hello.py Alice
```

In this example, the shell script will execute the `hello.py` script and pass the `Alice` argument to it.


Method 2: Add Shebang Line to Python Script
-------------------------------------------

Another way to execute a Python script from a shell script is to add a shebang line to the beginning of the Python script. A shebang line is the first line of a script file that tells the operating system what interpreter to use to run the script. For example, you can add the following shebang line to your Python script:

```python
#!/usr/bin/env python
```

This shebang line tells the operating system to use the `python` interpreter to execute the script. You can then make your Python script executable using the `chmod` command. For example:

```sh
chmod +x path/to/your_script.py
```

With this shebang line and executable permission, you can now call your Python script like any other executable program using its path. For example:

```sh
#!/bin/sh
path/to/your_script.py arg1 arg2 arg3
```


Method 3: Use subprocess Module in Python
-----------------------------------------

You can also execute a Python script from within a shell script by using the subprocess module in Python. The subprocess module allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. Here's an example of how to do this:

```python
#!/usr/bin/env python

import subprocess

subprocess.call(["python", "path/to/your_script.py", "arg1", "arg2", "arg3"])
```

In this example, we're calling the `subprocess.call()` function with a list of arguments. The first argument is a list of strings that represent the command and its arguments. The `subprocess.call()` function will execute this command and wait for it to complete. It will return the return code of the command.

Conclusion
----------

In this article, we've explored different ways to execute a Python program from within a shell script. You can call the Python interpreter directly, add a shebang line to your Python script, or use the subprocess module in Python. These methods give you flexibility depending on your needs and requirements.
