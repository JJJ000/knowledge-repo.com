---
title: What distinguishes subprocess.popen from os.system?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The subprocess.Popen allows for more control over a process while os.system simply executes a command in a subshell.
---

**Contents**

[TOC]

# Introduction
Python comes with built-in modules for interacting with the operating system. Among these modules, two modules are frequently used for executing commands in the operating system: `subprocess` and `os`. The `subprocess` module provides more advanced features for working with external processes than the `os` module. In this article, we will discuss the main differences between `subprocess.Popen()` and `os.system()` functions.

# os.system() Function
The `os.system()` function runs the command specified by the string argument in a subshell. The function waits until the command completes its execution, and then returns the exit status of the command. 

The `os.system()` function has some limitations. For example, it cannot capture the output of the command. Also, it cannot run a command asynchronously. The function is mainly suitable for running simple commands without much complexity. 

Here is an example of using the `os.system()` function to run a command:

```python
import os
os.system("dir")
```

In the above example, the `os.system()` function runs the `dir` command in the subshell and returns the exit code of the command.

# subprocess.Popen() Function
The `subprocess.Popen()` function provides more flexibility than the `os.system()` function. It can handle complex use cases, such as running a command asynchronously or capturing the output of the command. The function creates a new process to run the command.

The `subprocess.Popen()` function returns a `Popen` object that represents the new process. We can use this object to communicate with the new process or to wait for its completion. 

Here is an example of using the `subprocess.Popen()` function to run a command asynchronously:

```python
import subprocess
proc = subprocess.Popen("dir", shell=True)
# do other work while the command is executing
```

In the above example, the `subprocess.Popen()` function runs the `dir` command in the subshell and returns a `Popen` object representing the new process. The `shell=True` argument tells the function to invoke the command through the shell. We can do other work while the command is executing in the background.

# Differences between os.system() and subprocess.Popen() functions
Here are the main differences between the `os.system()` and `subprocess.Popen()` functions.

## Capturing output
The `os.system()` function cannot capture the output of the command. On the other hand, the `subprocess.Popen()` function provides several ways to capture the output:

- `proc.stdout.read()`: returns the output as a string
- `proc.stdout.readlines()`: returns the output as a list of lines
- `proc.communicate()`: returns a tuple of the output and error messages

## Asynchronous execution
The `os.system()` function runs the command synchronously, which means it waits until the command completes its execution. On the other hand, the `subprocess.Popen()` function can run the command asynchronously, which means it allows us to do other work while the command is executing.

## Handling errors
The `os.system()` function returns the exit status of the command, which is usually zero for success and non-zero for failure. On the other hand, the `subprocess.Popen()` function raises an exception if the command fails. We can catch the exception and handle the error in our code.

## Security concerns
The `os.system()` function runs the command in a subshell, which can be vulnerable to shell injection attacks. On the other hand, the `subprocess.Popen()` function is safer because it runs the command directly, without using the shell, unless we explicitly ask it to invoke the command through the shell (by setting `shell=True`). 

# Conclusion
The `os.system()` and `subprocess.Popen()` functions are both useful for running commands in the operating system from a Python program. However, the `subprocess.Popen()` function provides more flexibility and security features than the `os.system()` function. We should use the `os.system()` function only for simple use cases, and the `subprocess.Popen()` function for more advanced use cases.
