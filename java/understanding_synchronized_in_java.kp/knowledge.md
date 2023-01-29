---
title: What is the definition of 'synchronized'?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Java, `synchronized` is a keyword used to ensure that only one thread can access a method or block of code at a time.
---

**Contents**

[TOC]

### Definition

Synchronized is a keyword in Java that provides control over multiple threads accessing the same resources. It is used to ensure that only one thread can access a shared resource at a given time, thus avoiding race conditions.

### How it Works

When a thread enters a synchronized block of code, it acquires a lock on the object associated with the block. This lock is released only after the thread leaves the synchronized block. As long as the thread holds the lock, no other thread can enter the synchronized block.

### Advantages

Synchronized blocks in Java provide a mechanism for controlling access to shared resources in a multi-threaded environment. It ensures that only one thread can access a shared resource at a given time, thus avoiding race conditions.

### Disadvantages

Synchronized blocks can lead to performance issues due to the overhead of acquiring and releasing locks. In addition, it can lead to deadlocks if multiple threads attempt to acquire the same lock.
