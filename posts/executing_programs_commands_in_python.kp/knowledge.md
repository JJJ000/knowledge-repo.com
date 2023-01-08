---
title: What is the process for running a program or invoking a system command?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: You can execute a program or call a system command in Python using the `os.system()` function.
---

**Contents**

[TOC]

### Using the Subprocess Module

The subprocess module provides a consistent interface for creating and working with additional processes. It can be used to run external programs, such as shell commands and other applications, and collect their output.

### Using os.system()

The os.system() function allows you to execute a system command from within a Python script. It takes a single argument, which is the command to be executed, and returns the exit status of the command.

### Using os.popen()

The os.popen() function allows you to execute a command and read its output. It takes a single argument, which is the command to be executed, and returns a file object that can be used to read the output of the command.

### Using the Popen Constructor

The Popen constructor from the subprocess module allows you to execute a command and read its output. It takes a list of arguments, which is the command to be executed, and returns a Popen object that can be used to read the output of the command.
