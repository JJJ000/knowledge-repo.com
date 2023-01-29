---
title: What is the status of a concurrent list in java's jdk?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, the java.util.concurrent package contains several concurrent List implementations, such as ConcurrentLinkedQueue, CopyOnWriteArrayList, and ConcurrentSkipListSet.
---

**Contents**

[TOC]

### java.util.concurrent
Java includes a package of concurrent utilities, `java.util.concurrent`, which contains a variety of classes and interfaces for synchronizing concurrent access to shared data.

### java.util.concurrent.CopyOnWriteArrayList
One of the most commonly used classes from this package is `java.util.concurrent.CopyOnWriteArrayList`, which is a thread-safe implementation of the `java.util.List` interface.

### Benefits
This class provides several benefits over other thread-safe implementations of `List`, including:
- Improved scalability due to the copy-on-write strategy
- Improved performance due to the lack of synchronization overhead
- Improved thread safety due to the fact that all operations are atomic

### Drawbacks
The main drawback of using `CopyOnWriteArrayList` is that it is not suitable for applications that require frequent updates to the list, as the copy-on-write strategy can be expensive in terms of time and memory.
