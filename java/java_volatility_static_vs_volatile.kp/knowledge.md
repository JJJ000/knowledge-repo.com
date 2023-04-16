---
title: Comparing Java variables that are volatile and those that are static
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Volatile variables in Java are variables that can be changed by multiple threads, while static variables are variables that are shared across all instances of a class.
---

**Contents**

[TOC]

#Volatile

Volatile is a keyword in Java that is used to indicate that a variable's value will be modified by different threads. This keyword is used to make sure that all threads have the most up-to-date value of the variable.

#Static

Static is a keyword in Java that is used to indicate that a variable or method is a class variable or method, respectively. This means that it is associated with the class, rather than with an instance of the class. Static variables are also known as class variables.
