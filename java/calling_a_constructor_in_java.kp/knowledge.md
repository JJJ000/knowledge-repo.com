---
title: What is the process for invoking one constructor from another in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: You can call one constructor from another within a class by using the keyword `this` followed by the appropriate parameters.
---

**Contents**

[TOC]

### Defining Constructors
A constructor is a special method in a Java class that is used to initialize an object. It is called when an object is created and has the same name as the class. Constructors can take parameters to set initial values for the object's instance variables.

### Calling a Constructor from Another Constructor
When one constructor needs to call another constructor, the `this()` keyword can be used. The `this()` keyword is used to call another constructor in the same class. It must be the first statement in the constructor.

### Syntax
The syntax for calling one constructor from another is as follows:

```java
this(parameter list);
```

### Example
For example, if a class has two constructors, one with two parameters and one with three parameters, the two-parameter constructor can call the three-parameter constructor as follows:

```java
public MyClass(int a, int b) {
    this(a, b, 0);
}
```
