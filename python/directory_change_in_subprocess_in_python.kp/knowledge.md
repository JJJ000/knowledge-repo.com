---
title: Changing the directory of a subprocess
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To change directory in a subprocess module in Python, use the `cwd` argument while calling the `subprocess.run()` function.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, the subprocess module can be used to run external shell commands and scripts from within a Python script. One common task when working with subprocesses is changing the current working directory, which can be done using the `os.chdir()` or `subprocess.chdir()` commands. This article will explain how to change directories in Python subprocesses in more detail.

Section 2: Using os.chdir()
The `os.chdir()` function can be used to change the current working directory in a Python script. It takes a single argument, which is the path of the directory you want to change to, and returns None. Here is an example of how to use `os.chdir()` to change the working directory:

```python
import os

# Change the current working directory to '/path/to/directory'
os.chdir('/path/to/directory')
```

It is important to note that `os.chdir()` changes the working directory for the entire Python process, not just the subprocess that you are running. So if you change the working directory using `os.chdir()` in your main Python script, it will affect all subprocesses that you run.

Section 3: Using subprocess.Popen()
You can use `subprocess.Popen()` to create a new subprocess and execute a shell command or Python script in that subprocess. If you want to change the working directory of the new subprocess, you can use the `cwd` argument. Here is an example:

```python
import subprocess

# Create a new subprocess and change its working directory to '/path/to/directory'
subprocess.Popen(['ls', '-l'], cwd='/path/to/directory')
```

Note that the second argument to `subprocess.Popen()` is a list of arguments that will be passed to the shell command or script that you want to run. Here, we are running the `ls -l` command in the new subprocess.

Section 4: Using subprocess.check_output()
If you want to run a shell command or script and get its output as a string in your Python script, you can use `subprocess.check_output()`. This function works similarly to `subprocess.Popen()`, but it returns the output of the command or script as a string. Here is an example:

```python
import subprocess

# Run the 'ls' command in the '/path/to/directory' directory and get the output as a string
output = subprocess.check_output(['ls', '-l'], cwd='/path/to/directory')
print(output)
```

In this example, we are running the `ls -l` command in the `/path/to/directory` directory and printing its output to the console. The `cwd` argument is used to change the working directory of the new subprocess.
