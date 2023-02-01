---
title: What are the various Python exit commands and when should each one be employed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: There are many different exit commands in Python, such as exit(), quit(), sys.exit(), and os.\_exit(), which should all be used depending on the specific situation and context in which they are needed.
---

**Contents**

[TOC]

## exit()
The `exit()` command is used to exit the Python interpreter. It is the most basic exit command and should be used when you are done running the Python code and want to exit the interpreter.

## quit()
The `quit()` command is similar to `exit()` and is used to exit the Python interpreter. The difference between `exit()` and `quit()` is that `quit()` raises a `SystemExit` exception, which can be caught and handled.

## sys.exit()
The `sys.exit()` command is similar to `exit()` and `quit()` in that it is used to exit the Python interpreter. However, `sys.exit()` takes an optional argument which can be used to indicate an exit status. This can be used to indicate the success or failure of a program.

## os._exit()
The `os._exit()` command is used to exit the Python interpreter without calling any cleanup handlers or flushing any standard I/O buffers. This should only be used when it is absolutely necessary and should not be used in normal circumstances.
