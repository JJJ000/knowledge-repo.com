---
title: What is the c# equivalent of java's synchronized keyword?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In C#, the equivalent of Java`s synchronized keyword is the `lock` keyword.
---

**Contents**

[TOC]

### Lock

The C# language provides a `lock` keyword which behaves similarly to the Java `synchronized` keyword. The `lock` keyword is used to ensure that only one thread can access a particular block of code at any given time.

### Syntax

The syntax for the `lock` keyword is as follows:

```c#
lock (object)
{
    // code to be synchronized
}
```

Where `object` is the object to be locked.

### Usage

The `lock` keyword can be used to ensure that only one thread can access a particular block of code at any given time. This ensures that the code is executed in the correct order and that no race conditions occur.

### Benefits

Using the `lock` keyword provides several benefits. It ensures that data is not corrupted due to race conditions and it also ensures that threads are not blocked unnecessarily. This can improve the performance of an application by allowing threads to run in parallel.
