---
title: What does __pycache__ contain?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: \_\_pycache\_\_ is a folder created by Python to store compiled bytecode files for faster loading.
---

**Contents**

[TOC]

# What is __pycache__?
__pycache__ is a directory created when Python compiles source files. It contains the compiled bytecode of Python source files, which is used to improve the startup time of Python programs.

# What is Bytecode?
Bytecode is a representation of a program in a low-level language that is used by interpreters. It is a set of instructions that can be executed by a virtual machine or a real processor.

# What is the Purpose of __pycache__?
The __pycache__ directory is used to store the pre-compiled bytecode of Python modules. This helps to speed up the loading time of Python programs, as the bytecode can be loaded directly instead of being recompiled each time the program is run.

# What are the Benefits of __pycache__?
The benefits of __pycache__ include faster loading times, improved performance, and reduced memory usage. Additionally, it helps to ensure that the code is always up-to-date, as the bytecode is automatically re-compiled when the source code is changed.
