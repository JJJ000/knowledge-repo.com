---
title: What is the best way to initiate garbage collection in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Garbage collection can be forced in Java by calling System.gc() or Runtime.gc().
---

**Contents**

[TOC]

1. **Explicit Garbage Collection**

Garbage collection can be forced explicitly by calling the System.gc() method. This method is a hint to the JVM that it should run the garbage collector. The JVM can choose to ignore this request.

2. **System Properties**

The JVM can be configured to run garbage collection at certain intervals by setting system properties. The two properties that can be used to configure garbage collection are:

-XX:+ExplicitGCInvokesConcurrent

-XX:+ExplicitGCInvokesConcurrentAndUnloadsClasses

These properties can be set in the command line when starting the JVM.

3. **JMX**

Garbage collection can also be triggered using the Java Management Extensions (JMX). JMX provides a way to manage and monitor applications, system objects, services and devices.

Using JMX, the garbage collector can be triggered by calling the System.gc() method on the memoryMXBean object.

4. **Finalization**

The finalization process can be used to trigger garbage collection. The finalization process is a mechanism by which an object can perform some action before it is garbage collected. The finalization process can be used to force the JVM to run the garbage collector.
