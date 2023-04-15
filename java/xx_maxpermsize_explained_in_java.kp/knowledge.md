---
title: What is the purpose of the -xxmaxpermsize setting?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: -XXMaxPermSize sets the maximum size of the Permanent Generation memory, which is used to store class and method objects.
---

**Contents**

[TOC]

### Overview
-XX:MaxPermSize is a command line option for the Java HotSpot VM that sets the maximum size for the permanent generation memory. The permanent generation memory holds class and method objects.

### Benefits
Setting the maximum size for the permanent generation memory can help improve the performance of the Java HotSpot VM by preventing the memory from becoming too large, which can cause the application to become slow or unresponsive.

### Usage
The -XX:MaxPermSize command line option is used to set the maximum size for the permanent generation memory. The value is specified in bytes, and the default value is 64MB.

### Considerations
When setting the maximum size for the permanent generation memory, it is important to consider the amount of memory available on the system, as well as the size of the application. Setting the value too low can cause the application to throw an OutOfMemoryError, while setting it too high can lead to unnecessary memory usage.
