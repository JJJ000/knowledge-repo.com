---
title: What are the drawbacks of calling system.gc()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Calling System.gc() is bad practice because it can lead to unpredictable and inconsistent results, as the JVM may or may not choose to perform garbage collection.
---

**Contents**

[TOC]

1. Performance Impact 
    System.gc() is a costly operation and can cause a significant performance impact on the application. When System.gc() is called, the JVM will attempt to reclaim unused memory from the heap. This operation can cause a noticeable pause in the application, leading to a decrease in performance.

2. Unpredictable Results 
    System.gc() is not guaranteed to reclaim all unused memory and the results can be unpredictable. The JVM will attempt to reclaim memory, but the amount of memory reclaimed can vary from one call to the next.

3. Unnecessary Usage 
    System.gc() is typically not necessary and should only be used in special cases. The JVM will automatically perform garbage collection when needed, so calling System.gc() is often unnecessary.

4. Potential Memory Leaks 
    System.gc() can sometimes lead to memory leaks if it is not used properly. If objects are not properly released from memory, calling System.gc() will not reclaim the memory and can cause memory leaks.
