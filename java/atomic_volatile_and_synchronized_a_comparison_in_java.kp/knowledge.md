---
title: What are the distinctions between atomic, volatile, and synchronized?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Atomic variables are thread-safe and guarantee that all operations on them are atomic, volatile variables guarantee visibility of changes made by one thread to other threads, and synchronized blocks/methods guarantee exclusive access to a shared resource.
---

**Contents**

[TOC]

### Atomic
Atomic operations are operations that are guaranteed to be executed completely or not at all. Atomic operations are used to ensure that multiple threads do not access the same data at the same time, which can lead to data corruption. Atomic operations are often used to ensure that a single operation is completed before another operation is allowed to start.

### Volatile
Volatile variables are variables that are shared between multiple threads and can be modified by any of those threads. Volatile variables are used to ensure that the value of the variable is always up to date, even if multiple threads are accessing it.

### Synchronized
Synchronized blocks are used to ensure that only one thread can access a shared resource at a time. Synchronized blocks are used to prevent race conditions, which can lead to data corruption and other problems. Synchronized blocks are often used to ensure that critical sections of code are only executed by one thread at a time.
