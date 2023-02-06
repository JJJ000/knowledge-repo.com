---
title: Referencing the superclass constructor in Java using the super() keyword
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: super() is a reference to the immediate parent class of the class in which it is used, and is used to access the parent class`s methods and constructors.
---

**Contents**

[TOC]

### What is super()? 
`super()` is a keyword in Java that is used to refer to the parent class of the class in which it is used. It is used to access the constructors and methods of the parent class.

### How is super() Used?
`super()` is used to invoke the constructor of the parent class. It is generally used as the first line in the constructor of a subclass. It can also be used to access the methods of the parent class.

### When to Use super()
`super()` should be used when a constructor of the subclass needs to call the constructor of the parent class. It should also be used when a method of the subclass needs to call the method of the parent class.

### Benefits of super()
Using `super()` allows the subclass to access the methods and variables of the parent class. It also helps to reduce the amount of code that needs to be written in the subclass, as the methods and variables of the parent class can be accessed without having to rewrite them.
