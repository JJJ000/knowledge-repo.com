---
title: What is the default maximum value for the Java memory heap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The default max Java heap size is determined by the amount of physical memory available on the machine.
---

**Contents**

[TOC]

### Operating System
The default maximum Java heap size is determined by the amount of RAM available on the operating system. It is typically set to half of the available RAM. For example, if the system has 4GB of RAM, then the default maximum Java heap size will be 2GB.

### Java Version
The default maximum Java heap size is also determined by the version of Java being used. For example, Java 8 has a default maximum heap size of 1/4 of the available RAM, while Java 11 has a default maximum heap size of 1/2 of the available RAM.

### Garbage Collection
The default maximum Java heap size is also determined by the garbage collection algorithm being used. For example, the G1 garbage collector has a default maximum heap size of 1/4 of the available RAM, while the CMS garbage collector has a default maximum heap size of 1/2 of the available RAM.

### Other Factors
Other factors such as the amount of available disk space and the number of processors can also affect the default maximum Java heap size.
