---
title: What is the distinction between volatile and synchronized keywords in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Volatile is used to indicate that a variable`s value may be changed by multiple threads, while synchronized is used to control access to a shared resource by multiple threads.
---

**Contents**

[TOC]

### Volatile
Volatile is a keyword in Java that is used to indicate that a variable's value will be modified by different threads. When a field is declared volatile, the compiler and runtime are put on notice that this variable is shared and that operations on it should be performed in a thread-safe manner.

### Synchronized
Synchronized is a keyword in Java that is used to provide exclusive access to a shared resource. When a method is declared synchronized, it is given a lock that can only be acquired by one thread at a time. This ensures that only one thread can access the shared resource at any given time.

### Difference
The main difference between volatile and synchronized is that volatile is used to indicate that a variable's value will be modified by different threads, while synchronized is used to provide exclusive access to a shared resource. Volatile is a keyword that is used to provide thread-safety when accessing a shared variable, while synchronized is used to provide exclusive access to a shared resource.
