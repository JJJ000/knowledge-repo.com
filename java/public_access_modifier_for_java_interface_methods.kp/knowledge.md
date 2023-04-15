---
title: Do Java interface methods need to be declared with the public access modifier?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Methods in a Java interface should be declared with a public access modifier.
---

**Contents**

[TOC]

### Access Modifier
Methods in a Java interface should be declared with a public access modifier.

### Why
This is because all methods in an interface are implicitly public, and adding the public access modifier explicitly reinforces this.

### Benefits
Using the public access modifier makes the code more readable and easier to maintain. Additionally, it allows other developers to more easily understand the purpose of the interface and the methods it contains.

### Best Practices
It is considered best practice to declare methods in a Java interface with a public access modifier. This ensures that the code is clear and consistent, and that the interface is correctly used by other developers.
