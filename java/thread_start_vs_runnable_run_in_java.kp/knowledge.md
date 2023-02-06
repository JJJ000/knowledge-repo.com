---
title: What is the distinction between invoking thread's start() method and implementing runnable's run() method?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Thread start() creates a new thread and calls the run() method of the Thread, while Runnable run() is the method that is called when the thread is started.
---

**Contents**

[TOC]

## Thread start()
`Thread start()` is a method of the `Thread` class. It is used to start a new thread. When this method is called, the thread's `run()` method is automatically called.

## Runnable run()
`Runnable run()` is a method of the `Runnable` interface. It is used to execute the code in the `run()` method of a `Runnable` object. It is not used to start a new thread.
