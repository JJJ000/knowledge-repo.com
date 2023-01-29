---
title: Why is it necessary for the wait() method to be used inside of a synchronized block?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Wait() must always be in a synchronized block in Java to prevent any other threads from accessing the same object while it is waiting.
---

**Contents**

[TOC]

### Synchronized Blocks
Synchronized blocks are used to ensure that only one thread can access a shared resource at any given time. This is important to prevent race conditions and deadlocks.

### Wait() Method
The wait() method is used to pause the current thread until another thread calls notify() or notifyAll() on the same object. This is used to ensure that all threads have a chance to access a shared resource.

### Mutual Exclusion
Since the wait() method can cause a thread to pause, it must be used with caution. If it is not used in a synchronized block, then two or more threads may attempt to access the same resource at the same time, leading to race conditions and deadlocks.

### Conclusion
In order to ensure that only one thread can access a shared resource at any given time, the wait() method must always be used in a synchronized block in Java.
