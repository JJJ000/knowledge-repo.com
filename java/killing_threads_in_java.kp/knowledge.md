---
title: What is the process for terminating a thread in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Thread can be killed by calling its interrupt() method.
---

**Contents**

[TOC]

1. Using `interrupt()` Method
    - The `interrupt()` method can be used to interrupt a thread that is waiting or sleeping.
    - It sets the interrupted status of the thread to true, and throws an `InterruptedException` if the thread is blocked.
    - The `interrupt()` method should be used to interrupt the thread gracefully.

2. Using `stop()` Method
    - The `stop()` method is used to terminate the thread abruptly.
    - It is a deprecated method and should not be used in the production code.
    - The `stop()` method can cause the thread to lose its data which can lead to data corruption.
