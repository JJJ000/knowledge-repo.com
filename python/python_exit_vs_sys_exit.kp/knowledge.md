---
title: What is the distinction between exit() and sys.exit() in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: sys.exit() is used to exit the current program, while exit() is used to exit the current Python interpreter session.
---

**Contents**

[TOC]

# exit()

The `exit()` function is a part of the built-in `os` module in Python. It is used to exit the current program and return a status code to the operating system. It takes an optional argument, which is the status code that is returned to the operating system.

# sys.exit()

The `sys.exit()` function is a part of the built-in `sys` module in Python. It is used to exit the current program and return a status code to the operating system. It takes an optional argument, which is the status code that is returned to the operating system. Unlike `exit()`, `sys.exit()` raises the `SystemExit` exception, which can be caught and handled.
