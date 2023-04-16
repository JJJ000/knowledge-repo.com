---
title: The add() method of the Java list class throws an unsupportedoperationexception
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The List.add() method throws an UnsupportedOperationException if the list is immutable.
---

**Contents**

[TOC]

### What is List.add()?
List.add() is a method in the Java programming language that adds an element to the end of a list. It is part of the java.util.List interface, which is implemented by many classes, including ArrayList and LinkedList.

### What is UnsupportedOperationException?
UnsupportedOperationException is an exception thrown when an application attempts to use an unsupported operation on a data structure. This exception is thrown when an application attempts to modify a data structure, such as a list, in a way that is not supported by the underlying data structure.

### Why Does List.add() Throw UnsupportedOperationException?
List.add() can throw UnsupportedOperationException when the underlying list implementation does not support the add operation. This can occur when the list is read-only or when the list is backed by an immutable data structure, such as an array.

### How to Handle UnsupportedOperationException?
In order to handle UnsupportedOperationException, the application should check whether the list is read-only or backed by an immutable data structure before attempting to modify it. If the list is read-only, the application should create a new list that supports modifications. If the list is backed by an immutable data structure, the application should use a different data structure that supports modifications.
