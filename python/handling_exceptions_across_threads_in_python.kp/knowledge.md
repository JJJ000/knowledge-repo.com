---
title: Is it possible to handle an exception in the calling thread that occurred in a different thread while executing a specific thread's code?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `try/except` block in the caller thread to catch the exception raised by the target thread using the `Thread.join()` method.
---

**Contents**

[TOC]

# Catching a Thread's Exception in Python

When working with Python threads, it is necessary to handle exceptions raised by the threads. In this tutorial, we will look at how to catch a thread's exception in the caller thread.

## Section 1: Using the Thread.join() Method

One way to catch a thread's exception is by using the `Thread.join()` method. It simply waits for the thread to exit and re-raises any exception that was raised by the thread.

```python
import threading

def worker():
    # do some work
    raise Exception("Something went wrong")

t = threading.Thread(target=worker)
t.start()
t.join()  # Wait for the thread to exit

if t.is_alive():
    # The thread did not exit cleanly
    print("Thread did not exit cleanly")
else:
    # The thread exited cleanly
    print("Thread exited cleanly")
```

## Section 2: Using a Queue to Communicate Errors

Another way to catch a thread's exception is by using a `queue` to communicate between the threads. In this case, the worker thread will put any exception into a queue that the caller thread can then read from.

```python
import queue
import threading

def worker(q):
    try:
        # do some work
        raise Exception("Something went wrong")
    except Exception as e:
        q.put(e)

q = queue.Queue()
t = threading.Thread(target=worker, args=(q,))
t.start()

# Wait for the thread to exit
t.join()

# Check if there are any exceptions in the queue
while not q.empty():
    exception = q.get()
    print(f"Caught exception: {exception}")
```

## Section 3: Using a Callable Object

A third way to catch a thread's exception is by using a callable object that can be used as the `target` function for the thread. The callable object should have an `exception` attribute that will contain any exception raised by the thread.

```python
import threading

class Worker:
    def __init__(self):
        self.exception = None

    def __call__(self):
        try:
            # do some work
            raise Exception("Something went wrong")
        except Exception as e:
            self.exception = e

worker = Worker()
t = threading.Thread(target=worker)
t.start()

# Wait for the thread to exit
t.join()

if worker.exception:
    # There was an exception in the thread
    print(f"Caught exception: {worker.exception}")
else:
    # The thread exited cleanly
    print("Thread exited cleanly")
```

## Section 4: Conclusion

In this tutorial, we looked at three ways to catch a thread's exception in the caller thread. The first method is to use the `Thread.join()` method to wait for the thread to exit and re-raise any exceptions. The second method is to use a `queue` to communicate between the threads. The third method is to use a callable object that can be used as the `target` function for the thread. By using one of these methods, you can handle exceptions raised by a thread without allowing them to crash your program.
