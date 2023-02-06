---
title: What is the division of the Java memory pool?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Java memory pool is divided into separate areas for the heap, stack, and permanent generation.
---

**Contents**

[TOC]

1. **Heap Memory**: The heap is the runtime data area from which memory for all class instances and arrays is allocated. It is created when the JVM starts up and can increase or decrease in size.

2. **Non-Heap Memory**: Non-heap memory includes memory required for the internal processing or optimization for the JVM. This includes the memory for method area and memory required for the internal processing or optimization for the JVM such as garbage collection, compilation and loading of classes and methods.

3. **Code Cache**: Code cache is used to improve the performance of Java applications by storing the bytecode of the frequently used Java methods.

4. **PermGen Space**: The Permanent Generation (PermGen) space is used to store the metadata required by the JVM to describe the classes and methods used in the application. It is also used to store the String and various other class level data.
