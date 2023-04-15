---
title: Finding out the name of the method being executed
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The name of the currently executing method in Java can be retrieved using the `getMethodName()` method of the StackTraceElement class.
---

**Contents**

[TOC]

1. Using Reflection 

Reflection is a feature in the Java programming language. It allows an executing Java program to examine or "introspect" upon itself, and manipulate internal properties of the program. With the help of Reflection API, it is possible to get the name of the currently executing method. 

2. Using Thread 

Java Thread class provides two methods that can be used to get the name of the currently executing method. These methods are getStackTrace() and getName(). getStackTrace() returns an array of StackTraceElement objects, which contains the information about the currently executing method. getName() method returns the name of the thread. 

3. Using SecurityManager 

SecurityManager is a class in Java which provides the methods to check access, define the security policy etc. It also provides the getClassContext() method which can be used to get the name of the currently executing method. The getClassContext() method returns an array of Class objects representing the current execution stack. 

4. Using StackWalker 

StackWalker is a class introduced in Java 9 which provides the methods to walk the execution stack. It provides the getCallerClass() method which can be used to get the name of the currently executing method. The getCallerClass() method returns the Class object of the caller of the currently executing method.
