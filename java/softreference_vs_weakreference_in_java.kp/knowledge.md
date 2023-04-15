---
title: How do softreference and weakreference differ in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: SoftReference objects are cleared from memory only when the JVM needs to free up memory, whereas WeakReference objects are cleared from memory as soon as the garbage collector runs.
---

**Contents**

[TOC]

### SoftReference
SoftReference is a type of reference in Java which allows an object to be garbage collected only if JVM needs the memory. SoftReference objects are cleared at the discretion of the garbage collector in response to memory demand.

### WeakReference
WeakReference is another type of reference in Java which is similar to SoftReference but it is cleared by the garbage collector before SoftReferences. It allows an object to be garbage collected at any point of time, even if the memory is available.
