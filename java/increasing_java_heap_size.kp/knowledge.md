---
title: Increase the amount of memory allocated to the Java heap
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Increase the maximum heap size by using the -Xmx JVM option.
---

**Contents**

[TOC]

### Setting the Heap Size

The heap size in Java can be set by using the -Xmx flag when running a program. For example, to set the heap size to 1GB, the command would be:

`java -Xmx1024m <program_name>`

### Increasing the Heap Size

The heap size can be increased by increasing the value of the -Xmx flag. For example, to increase the heap size to 2GB, the command would be:

`java -Xmx2048m <program_name>`

### Maximum Heap Size

The maximum heap size is dependent on the amount of physical memory available on the system. Generally, the maximum heap size should not exceed 1/4th of the physical memory on the system.

### Setting the Heap Size Automatically

The heap size can also be set automatically by using the -XX:+UseG1GC flag. This flag allows the JVM to automatically adjust the heap size based on the amount of physical memory available on the system.
