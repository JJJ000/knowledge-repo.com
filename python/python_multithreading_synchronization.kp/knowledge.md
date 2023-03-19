---
title: Wait for all threads to finish in python's multithreading
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the join() method to wait until all threads are finished.
---

**Contents**

[TOC]

# Introduction
When working with multithreading in Python, it may become necessary to wait until all threads have completed before continuing execution. In this article, we will discuss how to do this by using various synchronization techniques provided by the `threading` module.

# Using `join()`
One way to wait for all threads to finish is by using the `join()` method. This method blocks the calling thread until the thread whose `join()` method is called has completed.

```python
import threading

def worker():
    # do some work here
    pass

threads = []

for i in range(5):
    t = threading.Thread(target=worker)
    threads.append(t)
    t.start()

# Wait for all threads to complete
for t in threads:
    t.join()

print("All threads have completed")
```

In the above example, we create 5 threads and start them. Then, we use a `for` loop to iterate over all threads and call `join()` on each of them. This means that the main thread will wait until all child threads have completed before printing "All threads have completed".

# Using a Barrier
Another way to wait for all threads to complete is by using a `Barrier` object. A `Barrier` is a synchronization primitive that allows a fixed number of threads to synchronize and wait for each other at a specific point.

```python
import threading

def worker(barrier):
    # do some work here
    barrier.wait()

threads = []
barrier = threading.Barrier(5)

for i in range(5):
    t = threading.Thread(target=worker, args=(barrier,))
    threads.append(t)
    t.start()

# Wait for all threads to complete
for t in threads:
    t.join()

print("All threads have completed")
```

In the above example, we create a `Barrier` object with a threshold of 5. This means that the `wait()` method will block until 5 threads have called it. In the `worker()` function, we call `wait()` after completing the work. This means that each thread will block until all other threads have called `wait()`. Finally, we use a `for` loop to iterate over all threads and call `join()` on each of them to wait for them all to complete.

# Using a Semaphore
A third way to wait for all threads to complete is by using a `Semaphore` object. A `Semaphore` is a synchronization primitive that controls access to a shared resource. It allows a fixed number of threads to access the shared resource simultaneously.

```python
import threading

def worker(semaphore):
    # do some work here
    semaphore.release()

threads = []
semaphore = threading.Semaphore(0)

for i in range(5):
    t = threading.Thread(target=worker, args=(semaphore,))
    threads.append(t)
    t.start()

# Wait for all threads to complete
for i in range(5):
    semaphore.acquire()

print("All threads have completed")
```

In the above example, we create a `Semaphore` object and initialize it with a value of 0. Each thread calls `release()` after completing the work, which increments the semaphore value. The main thread calls `acquire()` 5 times to decrement the semaphore value and waits until the value becomes 0. Finally, we print "All threads have completed" to indicate that all threads have finished executing.

# Conclusion
Waiting for all threads to complete can be achieved using various synchronization techniques provided by the `threading` module. The choice of technique depends on the specific problem and requirements of the program. The `join()`, `Barrier`, and `Semaphore` techniques discussed in this article can be used to ensure that all threads have completed before continuing execution.
