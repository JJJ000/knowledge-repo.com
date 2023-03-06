---
title: What is the method to designate the working directory for a subprocess?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `cwd` parameter in the `subprocess.Popen()` or `subprocess.run()` function to specify the working directory for a subprocess.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, subprocess module is used for spawning new processes, executing commands, and managing input/output streams. When using subprocess, we may need to specify the working directory for the new process. This can be done in several different ways.

Section 2: Using the cwd parameter
The most straightforward way to specify the working directory for a subprocess is to use the 'cwd' parameter when calling the subprocess.Popen() function. This parameter takes a string value that represents the path of the desired working directory. Here's an example:
```python
import subprocess

working_dir = "/path/to/working/directory"
cmd = "ls -l"

subprocess.Popen(cmd, cwd=working_dir)
```
In this example, we have specified the working directory for the 'ls' command as '/path/to/working/directory'.

Section 3: Using the chdir() function
Another way to change the working directory for a subprocess is to use the os.chdir() function before calling the subprocess. This function changes the current working directory of the Python process to the specified directory. Here's an example:
```python
import os
import subprocess

working_dir = "/path/to/working/directory"
cmd = "ls -l"

os.chdir(working_dir)
subprocess.Popen(cmd)
```
In this example, we have changed the working directory of the Python process to '/path/to/working/directory' using os.chdir(), and then we called the 'ls' command using subprocess.

Section 4: Using the shell=True parameter
Another way to specify the working directory for a subprocess is to use the shell=True parameter and include a 'cd' command in the command string. Here's an example:
```python
import subprocess

working_dir = "/path/to/working/directory"
cmd = "cd " + working_dir + " && ls -l"

subprocess.Popen(cmd, shell=True)
```
In this example, we have included a 'cd' command before the 'ls' command in the command string. When subprocess.Popen() is called with shell=True, the command string is executed using the system shell, which in this case will change the current working directory to '/path/to/working/directory' before executing the 'ls' command.
