---
title: Can you explain the global interpreter lock (gil) that is present in cpython?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The GIL is a mechanism used by the CPython interpreter to ensure that only one thread executes Python bytecode at a time.
---

**Contents**

[TOC]

### Introduction
CPython is an implementation of the popular programming language, Python. One of the features that distinguish CPython from other Python implementations is the global interpreter lock (GIL). This article briefly explains what the GIL is and its impact on multithreaded programming in CPython.

### What is the Global Interpreter Lock (GIL)?
The GIL is a mechanism in CPython that ensures that only one thread at a time can execute Python bytecode. In other words, it is a mutex that protects access to Python objects, preventing multiple threads from executing Python bytecode concurrently. The GIL is a feature of CPython's implementation and does not exist in other Python implementations, such as Jython or IronPython.

### Impact on Multithreaded Programming
The GIL has a significant impact on multithreaded programming in CPython. Since only one thread can execute Python bytecode at a time, multithreaded programs in CPython cannot fully utilize multiple cores and CPUs. Thus, the performance of multithreaded Python programs that spend most of their time executing Python code is often limited by the GIL. However, the GIL does not affect I/O-bound programs since they spend most of their time waiting for I/O and not executing Python bytecode.

### Workarounds
There are several workarounds to overcome the limitations imposed by the GIL. One solution is to use multiprocessing instead of multithreading. Since each process has its own interpreter and memory space, the GIL does not affect multiprocessing programs, and they can utilize multiple cores and CPUs efficiently. Another solution is to use alternative Python implementations that do not have a GIL, like Jython and IronPython. Finally, one can use C extension modules that release the GIL while performing CPU-bound tasks, allowing other threads to execute Python code concurrently.
