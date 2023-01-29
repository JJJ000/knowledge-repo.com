---
title: How does double brace initialization work in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Double Brace Initialization is a technique used to initialize an anonymous inner class in Java.
---

**Contents**

[TOC]

### Definition
Double Brace initialization is a technique used to initialize an anonymous inner class in Java. It is a shorthand way of creating an instance of an anonymous class that extends from a superclass or implements an interface.

### Syntax
The syntax for Double Brace initialization is as follows:

`new SuperclassOrInterface(){ 
 // code here 
}`

### Benefits
The primary benefit of Double Brace initialization is that it allows for the initialization of anonymous inner classes in a concise manner. It also allows for the initialization of anonymous inner classes with a single statement, which is useful for creating short and readable code.

### Drawbacks
The primary drawback of Double Brace initialization is that it can lead to memory leaks. This is because it creates an anonymous inner class that is not eligible for garbage collection, which can lead to memory leaks if it is not properly managed. Additionally, Double Brace initialization can lead to code that is difficult to read and understand.
