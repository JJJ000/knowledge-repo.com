---
title: What does the ellipsis (...) notation indicate for a parameter type in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Three dots next to a parameter type in Java indicate that the parameter is a variable length argument.
---

**Contents**

[TOC]

### Variable Arguments
The three dots next to a parameter type in Java indicate that the parameter is a variable argument. A variable argument is a parameter of a method that accepts an indefinite number of arguments. This type of parameter is also known as varargs.

### Syntax
The syntax for declaring a variable argument is to place three dots after the type of the parameter. For example:

```java
public void methodName(String... args) {
    // Method code here
}
```

### Usage
Variable arguments can be used when you do not know how many arguments are going to be passed to a method. The arguments passed to the method will be stored in an array. The array can then be iterated over and the individual elements can be accessed.
