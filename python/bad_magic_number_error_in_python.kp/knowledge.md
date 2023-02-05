---
title: What is the error code associated with the bad magic number?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The `bad magic number` error in Python is raised when attempting to import a file that was not created by the same version of Python.
---

**Contents**

[TOC]

# Definition
The bad magic number error in Python is an error that occurs when a byte-compiled file is created with an incorrect magic number. The magic number is a special number embedded in a compiled Python file that identifies the file type and version. When Python attempts to read a byte-compiled file with an incorrect magic number, it produces the bad magic number error.

# Causes
The bad magic number error is usually caused by attempting to read a file that was compiled with a different version of Python than the one being used to read it. It can also be caused by attempting to read a file that was compiled on a different platform than the one being used to read it. 

# Solutions
The simplest solution is to recompile the file with the same version of Python and the same platform. If that is not possible, then the file can be read in binary mode and the magic number can be manually updated.
