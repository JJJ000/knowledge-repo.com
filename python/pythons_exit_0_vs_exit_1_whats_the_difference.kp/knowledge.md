---
title: What is the distinction between exit(0) and exit(1) in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The exit(0) function call indicates successful termination of the program, whereas exit(1) indicates an unsuccessful termination of the program with an error.
---

**Contents**

[TOC]

# Overview

In Python, `exit(0)` and `exit(1)` are used to exit a program with a status code. The status code indicates the status of the program execution. 

# Exit Code

An exit code is a number that is returned by a program when it exits. An exit code of `0` indicates that the program exited normally without any errors, whereas a non-zero exit code indicates that the program encountered an error during execution. 

# exit(0)

`exit(0)` is used to exit a program normally. It indicates that the program completed execution without encountering any errors. 

For example, if a program completes a task successfully, it can exit using `exit(0)` to indicate that it completed the task without any errors. 

# exit(1)

`exit(1)` is used to exit a program when it encounters an error during execution. It indicates that the program encountered an error during execution and could not complete the task. 

For example, if a program encounters an exception or an error while performing a task, it can exit using `exit(1)` to indicate that it encountered an error during execution. 

# Conclusion

In summary, `exit(0)` is used to exit normally, indicating that the program completed execution without encountering any errors. `exit(1)` is used to exit when an error is encountered during execution, indicating that the program could not complete the task due to an error.
