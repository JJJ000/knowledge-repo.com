---
title: What is the best way to wait for all tasks to complete using an executorservice?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To wait for all tasks to finish in an ExecutorService, use the awaitTermination() method.
---

**Contents**

[TOC]

# 1. Create a CountDownLatch
A CountDownLatch allows a thread to wait until a set of operations being performed by other threads completes. To use a CountDownLatch, the main thread creates a latch with a given count and then each of the other threads uses the countDown() method to decrement the count when they complete. The main thread then calls await() on the latch which blocks until the count reaches zero.

# 2. Create a CyclicBarrier
A CyclicBarrier is similar to a CountDownLatch, but instead of waiting for a count to reach zero, it waits for a set of threads to all reach the same barrier. The main thread creates the barrier with a given count and then each of the other threads calls await() on the barrier. When the given number of threads have reached the barrier, they are all released and can continue.

# 3. Use ExecutorService.invokeAll()
The ExecutorService provides a way to wait for all tasks to finish by using the invokeAll() method. This method takes a collection of Callable objects and returns a list of Future objects. The main thread can then call the get() method on each of the Future objects to wait for the tasks to complete.

# 4. Use ExecutorService.shutdown()
The ExecutorService can also be used to wait for all tasks to finish by using the shutdown() method. This method will wait for all tasks to complete before returning. It is important to note that the shutdown() method will not wait for tasks that have already been submitted but not yet started.
