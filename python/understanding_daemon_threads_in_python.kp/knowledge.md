---
title: Explanation of threads that are daemonized
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Daemon threads are background threads that will be automatically terminated when the main program is exited.
---

**Contents**

[TOC]

# Introduction 

In Python, threads are used to run multiple tasks simultaneously. A threading module is used to create, manage, and manipulate threads in Python. A thread is a lightweight process that represents a single flow of execution. When a Python program starts, it creates a thread called the Main Thread. The Main Thread is responsible for creating additional threads that are started and managed by the Python Interpreter. Daemon Threads are a type of threads in Python that run in the background and do not prevent the program from exiting. 

# What are Daemon Threads?

Daemon Threads are a type of threads in Python that do not prevent the program from exiting when the Main Thread has finished. These threads run in the background and perform tasks such as cleaning up resources, monitoring events, or performing maintenance tasks. A daemon thread executes in the background and can be terminated abruptly by the Python Interpreter when the Main Thread has finished.

# How to create daemon threads in Python?

In Python, daemon threads are created using the setDaemon() method. This method is called on the thread object and takes a Boolean value as an argument. If the value is True, then the thread is a daemon thread, otherwise, it is a non-daemon thread. The setDaemon() method must be called before starting the thread using the start() method. 

Here is an example of how to create and use daemon threads in Python:

```
import threading, time

def worker():
    print('Daemon Started')
    time.sleep(5)
    print('Daemon Ended')

d = threading.Thread(target=worker)
d.setDaemon(True)

d.start()

print('Main Program Ended')
```

In this example, a daemon thread is created using the threading module. The worker function is called on the thread and executes for 5 seconds before exiting. The d.setDaemon(True) method sets the thread to a daemon thread, and the d.start() method starts the thread. The main program executes concurrently with the daemon thread until it reaches the end of the program and exits.

# Conclusion

Daemon Threads in Python are used to run tasks in the background that do not prevent the program from exiting. These threads are created using the setDaemon() method provided by the threading module. Daemon threads can be used to perform tasks such as cleaning up resources, monitoring events, or performing maintenance tasks. It’s important to note that daemon threads can be abruptly terminated by the Python Interpreter when the Main Thread has finished.
