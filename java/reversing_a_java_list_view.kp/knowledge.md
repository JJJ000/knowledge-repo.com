---
title: What is the process for reversing the order of items in a list in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To get a reversed list view on a list in Java, use the Collections.reverse() method.
---

**Contents**

[TOC]

# Section 1: Using Collections

Java's Collections framework provides a `Collections.reverse()` method that can be used to reverse a list. This method takes a list as its argument and returns a reversed list.

# Section 2: Iteration

Alternatively, you can iterate through the list, add each element to a new list in reverse order, and return the new list. This can be done with a `for` loop or a `while` loop.

# Section 3: Recursion

You can also use a recursive approach to reverse a list. This involves writing a recursive function that takes the list as its argument and returns the reversed list.

# Section 4: Streams

The Java 8 Streams API provides a `stream()` method that can be used to reverse a list. This method takes a list as its argument and returns a reversed list.
