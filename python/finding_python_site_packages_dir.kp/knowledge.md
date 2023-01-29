---
title: Where is my Python site-packages directory located?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The location of the Python site-packages directory can be found by running `python -m site` in the command line.
---

**Contents**

[TOC]

## Using the Command Line
1. Open the command line.
2. Enter the command `python -m site --user-site`.
3. The output of this command will be the path to the Python site-packages directory.

## Using the Python Interpreter
1. Open the Python interpreter.
2. Enter the command `import site; site.getsitepackages()`.
3. The output of this command will be a list of paths to the Python site-packages directory.
