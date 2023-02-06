---
title: Is there a limit to the size of a Java array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, Java arrays have a maximum size that is determined by the amount of memory available.
---

**Contents**

[TOC]

### Yes
Java arrays have a maximum size of `Integer.MAX_VALUE`, which is 2^31 - 1.

### No
Java arrays do not have a maximum size that is enforced by the language, but there is a practical limit due to the amount of memory available on the system. When an array is created, it is allocated a certain amount of memory. If the array grows beyond the allocated memory, the Java Virtual Machine (JVM) will throw an OutOfMemoryError.

### Limitations
The maximum size of an array also depends on the platform and the implementation of the JVM. For example, some implementations may limit the maximum size of an array to 2^31 - 1 elements, while others may allow up to 2^32 - 1 elements.

### Conclusion
Java arrays do not have an enforced maximum size, but there is a practical limit due to the amount of memory available on the system. The maximum size of an array also depends on the platform and the implementation of the JVM.
