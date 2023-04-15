---
title: Executing code in the primary thread from a different thread
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is not possible to directly run code in the main thread from another thread in Java.
---

**Contents**

[TOC]

### Overview
When programming in Java, it is often necessary to run code in the main thread from another thread. This can be done using a few different methods, such as using the Thread.join() method, the ExecutorService class, or the Future class.

### Thread.join() Method
The Thread.join() method allows a thread to wait for another thread to finish its execution before continuing. This can be used to ensure that code in the main thread is executed after code in the other thread has finished running.

### ExecutorService Class
The ExecutorService class provides an interface for submitting tasks to be executed by a thread pool. This allows code in the main thread to be executed after the tasks in the thread pool have finished running.

### Future Class
The Future class allows a thread to wait for the result of a computation that is running in another thread. This can be used to ensure that code in the main thread is executed after the computation in the other thread has finished running.
