---
title: What is the definition of 'atomic' in programming?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Java, `atomic` refers to an operation that is performed as a single, indivisible unit, meaning that the operation will either complete in its entirety or not at all.
---

**Contents**

[TOC]

### Definition

Atomic in programming in Java refers to an operation that is performed as a single, indivisible unit. This means that the operation either happens completely, or not at all, and no intermediate state is possible.

### Examples

A common example of an atomic operation in Java is a read-write lock. In this case, the operation of writing to a file is done in a single, indivisible unit. If the operation is interrupted, the data is not written to the file, and the file remains unchanged.

Another example is a transaction in a database. Here, a single operation is performed as a single unit, such that all the changes made to the database are either committed or rolled back as a single unit.

### Benefits

Atomic operations are useful because they guarantee that the operation is performed in a consistent and reliable way. This is especially important in applications that involve multiple threads, as it ensures that each thread can access the data without interference from other threads. This helps to ensure that the data remains consistent and reliable.
