---
title: What is the procedure for determining if the current thread is not the main thread?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use Thread.currentThread() and compare it to Thread.mainThread().
---

**Contents**

[TOC]

1. Using `Thread.currentThread()`
   
   The `Thread.currentThread()` method can be used to get the current thread. By comparing the current thread to the main thread, we can determine whether the current thread is not the main thread.

2. Comparing Thread IDs
   
   The `getId()` method can be used to get the ID of the current thread. By comparing the ID of the current thread to the ID of the main thread, we can determine whether the current thread is not the main thread.

3. Using `Thread.isMainThread()`
   
   The `Thread.isMainThread()` method can be used to determine if the current thread is the main thread. If the method returns `false`, then the current thread is not the main thread.

4. Using `Thread.isDaemon()`
   
   The `Thread.isDaemon()` method can be used to determine if the current thread is a daemon thread. If the method returns `false`, then the current thread is not a daemon thread and thus is not the main thread.
