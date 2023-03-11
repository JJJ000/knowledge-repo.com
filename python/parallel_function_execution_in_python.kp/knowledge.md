---
title: What is the process for executing functions simultaneously?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the Python multiprocessing module to run functions in parallel.
---

**Contents**

[TOC]

#### Introduction

Python is one of the most popular programming languages, which is capable of running multiple tasks in parallel. Running functions in parallel means executing multiple tasks at the same time, which can significantly reduce the execution time of the code. In this tutorial, we will explore different ways of running functions in parallel in Python.

#### Using the threading module

One of the simplest ways of running functions in parallel is by using the `threading` module. This module provides a way to create threads, which are small units of execution that can run concurrently with other threads. To use the `threading` module, we need to create a `Thread` object for each function that we want to run in parallel. Here is an example:

```python
import threading

def func1():
    # some code here

def func2():
    # some code here

t1 = threading.Thread(target=func1)
t2 = threading.Thread(target=func2)

t1.start()
t2.start()

t1.join()
t2.join()
```

In the above example, we create two threads, `t1` and `t2`, each with a target function `func1` and `func2`, respectively. We start the threads using the `start()` method, and wait for them to finish using the `join()` method.

#### Using the multiprocessing module

Another way of running functions in parallel is by using the `multiprocessing` module. This module provides a way to create separate processes, each with its own memory space, that can run concurrently with other processes. To use the `multiprocessing` module, we need to create a `Process` object for each function that we want to run in parallel. Here is an example:

```python
import multiprocessing

def func1():
    # some code here

def func2():
    # some code here

p1 = multiprocessing.Process(target=func1)
p2 = multiprocessing.Process(target=func2)

p1.start()
p2.start()

p1.join()
p2.join()
```

In the above example, we create two processes, `p1` and `p2`, each with a target function `func1` and `func2`, respectively. We start the processes using the `start()` method, and wait for them to finish using the `join()` method.

#### Using the concurrent.futures module

The `concurrent.futures` module provides a way to run functions in parallel using high-level interfaces such as `ThreadPoolExecutor` and `ProcessPoolExecutor`. These interfaces manage the creation and destruction of threads or processes for us, and provide a simple interface that we can use to submit functions for execution. Here is an example:

```python
import concurrent.futures

def func1():
    # some code here

def func2():
    # some code here

with concurrent.futures.ThreadPoolExecutor() as executor:
    f1 = executor.submit(func1)
    f2 = executor.submit(func2)

    result1 = f1.result()
    result2 = f2.result()
```

In the above example, we create a `ThreadPoolExecutor` object, which manages a pool of threads for us. We submit the `func1` and `func2` functions for execution using the `submit()` method. The `result()` method is used to retrieve the results of the function calls.

#### Conclusion

In this tutorial, we explored different ways of running functions in parallel in Python. We learned how to use the `threading` module to create threads, the `multiprocessing` module to create processes, and the `concurrent.futures` module to run functions using high-level interfaces. By using these techniques, we can significantly reduce the execution time of our code and improve its performance.
