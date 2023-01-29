---
title: What are .pyc files if Python is an interpreted language?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: .pyc files are compiled bytecode files created by the Python interpreter.
---

**Contents**

[TOC]

#Overview
.pyc files are Python bytecode files that are generated when Python source files are compiled. They contain the compiled bytecode of Python source files, which is used to improve the performance of Python programs.

#What is Python Bytecode?
Python bytecode is the lower-level form of the Python code that is generated when a Python source file is compiled. It is a collection of instructions that can be executed by the Python Virtual Machine (PVM). The PVM is responsible for executing the bytecode instructions, which are represented as numbers.

#What are .pyc Files?
.pyc files are created when Python source files are compiled. They contain the compiled bytecode of the Python source file, which is used to improve the performance of Python programs. The .pyc files are stored in the same directory as the corresponding .py files, and are updated whenever the .py files are modified.

#Benefits of .pyc Files
The main benefit of .pyc files is that they can improve the performance of Python programs. By compiling the source code into bytecode, the PVM can execute the instructions more quickly. This can result in faster program execution and improved performance. Additionally, .pyc files can help to reduce the amount of time it takes to start a program, since the bytecode is already compiled and ready to be executed.
