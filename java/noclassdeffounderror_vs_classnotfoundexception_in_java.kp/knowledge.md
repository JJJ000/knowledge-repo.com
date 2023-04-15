---
title: What are the causes of, and differences between, noclassdeffounderror and classnotfoundexception?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: NoClassDefFoundError occurs when a class is present at compile time but is missing at runtime, while ClassNotFoundException occurs when a class is not found during the execution of a program.
---

**Contents**

[TOC]

####NoClassDefFoundError
NoClassDefFoundError is an error that occurs when a class is present at compile time but not available at runtime. This can happen when classes or their dependencies are missing from the classpath.

####ClassNotFoundException
ClassNotFoundException is an exception that occurs when a class is not found during a Class.forName() method call. This can happen when the class name is incorrect or the class is not in the classpath.

####Differences
NoClassDefFoundError indicates that the class was present at compile time, but not at runtime. ClassNotFoundException indicates that the class was not found during a Class.forName() method call.
