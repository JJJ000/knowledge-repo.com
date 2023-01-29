---
title: Examples of the gang of four design patterns found in java's core libraries
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Observer Pattern is used in Java`s Observable and Observer classes.
---

**Contents**

[TOC]

### Factory Pattern
The Factory Pattern is used to create objects without exposing the creation logic to the client and refer to the newly created object using a common interface. 

Examples of this pattern can be found in the Java core libraries in the java.util.Calendar and java.util.ResourceBundle classes.

### Observer Pattern
The Observer Pattern is used to allow an object to publish changes to its state. Other objects subscribe to be immediately notified of any changes. 

Examples of this pattern can be found in the Java core libraries in the java.util.Observable and java.util.Observer classes.

### Singleton Pattern
The Singleton Pattern is used to ensure that only one instance of a class is created. 

Examples of this pattern can be found in the Java core libraries in the java.lang.Runtime and java.awt.Desktop classes. 

### Command Pattern
The Command Pattern is used to encapsulate a request as an object, thereby allowing for the parameterization of clients with different requests, and the queuing or logging of requests. 

Examples of this pattern can be found in the Java core libraries in the java.lang.Runnable and java.util.concurrent.Callable classes.
