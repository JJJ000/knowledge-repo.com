---
title: What is the exact purpose of the jvm option -xss?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: -Xss sets the maximum Java thread stack size, which controls the amount of memory allocated to each thread.
---

**Contents**

[TOC]

## Overview

The -Xss JVM option is used to set the thread stack size in Java. It is used to limit the amount of memory a thread can use for its stack. By setting the thread stack size, the JVM can ensure that the thread does not consume too much memory.

## Benefits

Using the -Xss option can help improve the performance of the JVM by reducing the amount of memory that a thread can consume. It can also help to reduce the amount of memory used by the JVM, which can help to reduce the overall memory usage of the application.

## Usage

The -Xss option can be used to set the thread stack size in Java. The syntax for setting the thread stack size is:

`java -Xss<size>`

Where <size> is the thread stack size in bytes. For example, to set the thread stack size to 256K, you can use the following command:

`java -Xss256K`

## Limitations

The -Xss option can only be used to set the thread stack size in Java. It cannot be used to set the heap size, garbage collection parameters, or other JVM parameters. In addition, setting the thread stack size too low can cause the JVM to crash. Therefore, it is important to set the thread stack size carefully.
