---
title: What is the distinction between the wait() and sleep() methods in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: `wait()` is used to pause the execution of a thread until another thread notifies it, while `sleep()` is used to pause the execution of a thread for a specified amount of time.
---

**Contents**

[TOC]

**wait()**

- Definition: 
wait() is a method of the Object class which causes the current thread to wait until another thread invokes the notify() method or the notifyAll() method for this object.

- Usage:
wait() is used in Java when a thread needs to wait for another thread to finish its task before continuing.

**sleep()**

- Definition: 
sleep() is a static method of the Thread class which causes the currently executing thread to sleep for the specified number of milliseconds.

- Usage:
sleep() is used in Java when a thread needs to pause execution for a specified amount of time before continuing.
