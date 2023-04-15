---
title: What are the similarities and differences between the runnable and callable interfaces in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Runnable is used to execute code in a thread, while Callable is used to return a result from a thread.
---

**Contents**

[TOC]

#Runnable Interface
The Runnable interface is a functional interface that contains only one abstract method: run(). It is used to represent a task that can be executed by a thread. The Runnable interface is used to create a thread by passing an instance of the class implementing this interface to the Thread constructor.

#Callable Interface
The Callable interface is a functional interface that contains a single abstract method: call(). It is used to represent a task that returns a result and may throw an exception. The Callable interface is used to create a thread by passing an instance of the class implementing this interface to the ExecutorService.submit() method. The result of the task can be obtained by calling the Future.get() method.
