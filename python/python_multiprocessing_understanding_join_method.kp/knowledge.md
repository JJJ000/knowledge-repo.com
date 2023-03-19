---
title: Could you explain the functionality of the .join() method in the Python multiprocessing module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The Python multiprocessing module`s .join() method waits for all processes to complete before moving on to the next instructions.
---

**Contents**

[TOC]

## Introduction
The Python multiprocessing module's `.join()` method is used to synchronize the execution of multiple processes. In other words, it allows a program to wait until all the child processes have completed their execution before proceeding with the rest of the code. 

## Usage
When a program spawns multiple processes using the multiprocessing module, each process becomes an independent entity with its own memory space, instruction pointer, and execution stack. The parent process may not know when each child process has completed its execution. This is where the `.join()` method comes into play. 

The `.join()` method is called on a `Process` object, which represents a child process. The parent process then waits until the child process has completed its execution, and only then does it proceed with the rest of the code. 

## Example
Consider the following code snippet that spawns a child process and waits for it to complete using the `.join()` method.

```python
import multiprocessing
import time

def worker():
    print("Starting worker")
    time.sleep(2)
    print("Worker completed")

if __name__ == '__main__':
    p = multiprocessing.Process(target=worker)
    p.start()
    p.join()

    print("Parent process completed")
```

In this example, a child process (represented by the `worker` function) is spawned using the `Process` object from the multiprocessing module. The parent process then waits for the child process to complete using the `.join()` method. Finally, the parent process prints a message indicating that it has completed its execution. 

When this program is run, the output will be as follows:

```
Starting worker
Worker completed
Parent process completed
```

Note that the parent process continues with the rest of the code only after the child process has completed its execution.

## Conclusion
In summary, the Python multiprocessing module's `.join()` method is used to synchronize the execution of multiple processes. It allows the parent process to wait until a child process has completed its execution before proceeding with the rest of the code. The `.join()` method is called on a `Process` object and blocks the parent process until the child process has completed its execution.
