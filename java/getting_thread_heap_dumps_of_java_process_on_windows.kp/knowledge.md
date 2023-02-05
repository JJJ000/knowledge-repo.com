---
title: How can a thread and heap dump of a Java process on windows be obtained if it is not running in a console?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use a tool such as jstack or jmap to get a thread and heap dump of a Java process on Windows that is not running in a console.
---

**Contents**

[TOC]

## Using VisualVM
1. Download and install VisualVM from the [Oracle website](https://visualvm.github.io/download.html).
2. Start VisualVM and locate the Java application process in the Applications tab.
3. Right-click on the process and select "Thread Dump" or "Heap Dump" to generate the thread and heap dumps.

## Using JConsole
1. Download and install JConsole from the [Oracle website](https://www.oracle.com/technetwork/java/javase/downloads/index.html).
2. Start JConsole and locate the Java application process in the Applications tab.
3. Right-click on the process and select "Thread Dump" or "Heap Dump" to generate the thread and heap dumps.

## Using jcmd
1. Download and install the Java Development Kit (JDK) from the [Oracle website](https://www.oracle.com/technetwork/java/javase/downloads/index.html).
2. Open a command prompt and type the following command to get the process ID (PID) of the Java application process: `jps -l`
3. Once you have the PID, type the following command to generate the thread dump: `jcmd <PID> Thread.print`
4. To generate the heap dump, type the following command: `jcmd <PID> GC.heap_dump <filename>.hprof`
