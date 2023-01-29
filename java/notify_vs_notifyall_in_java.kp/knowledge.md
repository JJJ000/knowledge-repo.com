---
title: What is the difference between notify() and notifyall() in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: notify() wakes up a single thread that is waiting on the object, while notifyAll() wakes up all threads waiting on the object.
---

**Contents**

[TOC]

### notify()

The `notify()` method wakes up a single thread that is waiting on this object's monitor. If any threads are waiting on this object, one of them is chosen to be awakened. The choice is arbitrary and occurs at the discretion of the implementation.

### notifyAll()

The `notifyAll()` method wakes up all threads that are waiting on this object's monitor. A thread waits on an object's monitor by calling one of the `wait()` methods.

### Difference between notify() and notifyAll()

The primary difference between `notify()` and `notifyAll()` is that `notify()` wakes up a single thread, while `notifyAll()` wakes up all threads that are waiting on the object's monitor.

### When to use notify() vs. notifyAll()

`notify()` should be used when you only want to wake up one thread, while `notifyAll()` should be used when you want to wake up all threads. It is important to note that using `notify()` instead of `notifyAll()` can result in deadlocks, so it is important to understand when to use each method.
