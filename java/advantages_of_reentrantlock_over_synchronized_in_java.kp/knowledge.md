---
title: What are the advantages of using a reentrantlock over using the synchronized keyword on an object?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: ReentrantLock allows for more complex synchronization logic than synchronized(this), such as timed waits and multiple condition variables.
---

**Contents**

[TOC]

1. **Mutual Exclusion**
  Both synchronized and ReentrantLock provide mutual exclusion, meaning that only one thread can access a shared resource at a time.

2. **Fairness**
  ReentrantLock provides the ability to specify the fairness policy, whereas synchronized blocks do not. Fairness policy determines the order in which threads waiting for the lock will be granted access.

3. **Timeout**
  ReentrantLock provides the ability to specify a timeout when acquiring a lock, whereas synchronized blocks do not. This allows the thread to move on to other tasks if the lock is not acquired within the specified time.

4. **Interruptible Lock**
  ReentrantLock provides the ability to interrupt a thread that is waiting to acquire a lock, whereas synchronized blocks do not. This allows the thread to respond to interrupts and take appropriate action.
