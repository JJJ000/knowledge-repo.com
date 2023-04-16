---
title: The difference between a volatile boolean and an atomic boolean
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: An AtomicBoolean is a thread-safe boolean primitive, while a Volatile boolean is a non-thread-safe boolean primitive that can be modified from multiple threads.
---

**Contents**

[TOC]

### Volatile Boolean
A volatile boolean is a boolean primitive type that is declared with the volatile keyword. This keyword ensures that the value of the boolean is always up-to-date and can be accessed by multiple threads. The volatile keyword also ensures that the boolean is not cached in any thread-local memory and is always read from main memory.

### AtomicBoolean
An AtomicBoolean is a boolean primitive type that is declared with the AtomicBoolean class. This class provides atomic operations on boolean values and ensures that the boolean is always up-to-date and can be accessed by multiple threads. The AtomicBoolean class also provides atomic operations on the boolean such as compare and set, get and set, and etc.

### Difference
The main difference between a volatile boolean and an AtomicBoolean is that the volatile boolean does not provide any atomic operations on the boolean whereas the AtomicBoolean provides atomic operations on the boolean. This means that the AtomicBoolean is more reliable and efficient to use when working with multiple threads.
