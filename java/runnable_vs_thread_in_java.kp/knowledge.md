---
title: What are the differences between `implements runnable` and "extends thread" in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Implementing Runnable allows for the creation of multiple threads from a single object, while extending Thread creates a single thread from a class.
---

**Contents**

[TOC]

### Implements Runnable
The Runnable interface should be implemented by any class whose instances are intended to be executed by a thread. The class must define a method of no arguments called run. This interface is designed to provide a common protocol for objects that wish to execute code while they are active.

### Extends Thread
Thread is a class which extends Object and implements Runnable interface. It has constructors and methods which are used to create and perform operations on a thread. By extending Thread class, the class can override the run() method to define the code which the thread will execute. The thread can then be started by calling the start() method.
