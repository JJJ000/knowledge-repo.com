---
title: What is the process for re-installing an updated version of a package in the Python interpreter?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the `reload` function to re-import an updated package while in the Python Interpreter.
---

**Contents**

[TOC]

# Method 1: Restarting Python Interpreter

1. Exit the current Python interpreter session.
2. Re-open the Python interpreter.
3. Import the updated package.

# Method 2: Reloading the Package

1. Use the `reload()` function from the `importlib` module to reload the package.
2. Call the `reload()` function, passing in the package name as an argument.
3. The package will be reloaded with the updated version.
