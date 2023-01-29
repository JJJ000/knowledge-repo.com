---
title: A variable that is not static cannot be accessed from a static context
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Non-static variables must be instantiated in an object in order to be referenced from a static context.
---

**Contents**

[TOC]

### What is a static context?

In Java, a static context refers to a code block in which all variables and methods are static. This means that all variables and methods must be declared with the 'static' keyword, and can only be accessed directly from the class, rather than from an instance of that class.

### What is a non-static variable?

A non-static variable is a variable that is declared without the 'static' keyword. It is associated with an instance of a class, and can only be accessed from an instance of that class.

### Why can't a non-static variable be referenced from a static context?

Since a static context can only access static variables and methods, it cannot access non-static variables. This is because non-static variables are associated with a specific instance of a class, and the static context does not have access to any instances of the class.

### What are the alternatives?

The alternative to referencing a non-static variable from a static context is to use a static method to access the non-static variable. This can be done by creating a static method that takes an instance of the class as a parameter, and then accessing the non-static variable from within that method.
