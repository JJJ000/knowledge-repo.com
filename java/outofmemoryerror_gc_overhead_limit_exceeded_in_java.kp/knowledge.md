---
title: The Java virtual machine has run out of memory due to excessive garbage collection activity exceeding the limit
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The GC overhead limit exceeded error occurs when the garbage collector spends too much time trying to free up memory.
---

**Contents**

[TOC]

### Overview
Java's `OutOfMemoryError` is thrown when an application attempts to use more memory than is available in the Java Virtual Machine (JVM). The `GC overhead limit exceeded` error is a specific type of `OutOfMemoryError` that occurs when too much time is spent performing garbage collection and not enough heap space is freed up.

### Causes
The `GC overhead limit exceeded` error can occur when the JVM spends more than 98% of its time performing garbage collection and is unable to free up 2% of the heap. This can happen when the application creates too many objects and the garbage collector is unable to keep up with the demand. Additionally, the garbage collector may be unable to reclaim memory from objects that are still in use.

### Solutions
The first step in solving the `GC overhead limit exceeded` error is to identify the cause. This can be done by using a profiler to identify the objects that are taking up the most memory and which are no longer needed. Once the cause is identified, the application can be optimized to reduce the number of objects being created and/or to reclaim memory from objects that are no longer in use.

It is also possible to increase the JVM heap size to give the garbage collector more space to work with. However, this should only be done as a last resort, as it can lead to performance issues if the application is not optimized properly.
