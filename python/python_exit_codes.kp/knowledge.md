---
title: Changing the phrasing of 'exit codes in python' could be 'python exit codes'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python, a program typically exits with a 0 exit code to indicate successful completion, and a non-zero exit code to indicate an error.
---

**Contents**

[TOC]

# Successful Exit Code
A successful exit code in Python is a code that is returned to the operating system when a program is executed successfully. The most common successful exit code is 0.

# Unsuccessful Exit Code
An unsuccessful exit code in Python is a code that is returned to the operating system when a program fails to execute. Common unsuccessful exit codes include 1, 2, and 3.

# Custom Exit Codes
Python also allows users to create custom exit codes. These codes can be used to indicate a specific error or to provide additional information about the program's execution.

# Exiting Python Scripts
When exiting a Python script, it is important to use the sys.exit() function. This function will ensure that the correct exit code is returned to the operating system.
