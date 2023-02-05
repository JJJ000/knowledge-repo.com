---
title: What is the purpose of the java.lang.thread.interrupt() method?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: java.lang.Thread.interrupt() interrupts the thread, causing it to throw an InterruptedException.
---

**Contents**

[TOC]

# Definition
Java.lang.Thread.interrupt() is a method used to interrupt a thread that is currently waiting, sleeping, or is otherwise occupied.

# Usage
This method is used to interrupt a thread that is currently in a blocking operation such as a wait(), join(), or sleep() call. When the interrupt() method is called on a thread, the thread will throw an InterruptedException. 

# Benefits
Using this method can help improve the performance of a program by allowing threads to be interrupted and freed up to perform other tasks. Additionally, it can be used to terminate a thread that is no longer needed.

# Considerations
When using this method, it is important to be aware that the interrupted thread may still be in the process of completing its current task. Therefore, it is important to take this into consideration when using this method. Additionally, it is important to be aware that this method will not stop a thread that is already running.
