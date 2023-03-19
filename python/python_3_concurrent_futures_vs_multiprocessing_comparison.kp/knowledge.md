---
title: The comparison of concurrent.futures and multiprocessing in Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Concurrent.futures is a higher-level abstraction for asynchronous execution of tasks and multiprocessing is a lower-level library for executing subprocesses that can run in parallel.
---

**Contents**

[TOC]

Introduction

Python has two primary modules to support parallelism and concurrency, the concurrent.futures and multiprocessing modules. However, developers often have a difficult time choosing between them. While both modules achieve similar functionality, they have distinct approaches and syntax that affect their performance and implementation in the code. 

This article aims to shed some light on the similarities and differences between the two modules, and how to choose the most suitable one for your use case.

Section 1: The purpose of the Concurrent.futures and Multiprocessing modules

The concurrent.futures module was introduced in Python 3.2 to support asynchronous programming with a consistent API. The module provides a high-level interface for asynchronously executing functions and methods using threads or processes via an executor pool.

On the other hand, the multiprocessing module is designed explicitly to execute Python code using multiple processes to circumvent the Global Interpreter Lock (GIL). It supports parallelism by addressing multiple CPUs or cores of a computer system.

Section 2: Differences between Concurrent.futures and Multiprocessing

The key difference between concurrent.futures and multiprocessing is their approach to parallelism. While concurrent.futures relies on threads or processes managed by the threaded or process pools, multiprocessing creates separate processes to run the tasks.

Some other essential differences are:

1. Performance: Both modules have a comparable runtime performance for CPU-bound tasks that exceed the GIL's limitations. However, in I/O-bound tasks or tasks that require a lot of communication between processes, concurrent.futures outperforms multiprocessing.

2. Syntax: concurrent.futures has a higher-level and simpler interface compared to the multiprocessing. The concurrent.futures Executor class has two subclasses that are easy to use - ThreadPoolExecutor and ProcessPoolExecutor.

3. Portability: concurrent.futures is more portable than the multiprocessing module. Concurrent.futures can be used in many platforms, including Windows and Linux, while multiprocessing is restricted to UNIX-like systems.

Section 3: Choosing between Concurrent.futures and Multiprocessing

The choice between concurrent.futures and multiprocessing ultimately depends on the specific use case. 

If the task requires a high level of communication between processes, such as sharing data or communication during the execution, the concurrent.futures module is more efficient.

If the task only requires maximum performance and computational power without the need for inter-process communication, multiprocessing is an excellent choice.

Section 4: Conclusion

Concurrent.futures and multiprocessing modules are essential for achieving maximum efficiency in Python programs. Understanding the specifics of each module's functionality, performance, and syntax is critical in determining the best option for a given task.
