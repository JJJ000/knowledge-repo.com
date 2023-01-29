---
title: Can the instanceof operator be used in a switch statement?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, the instanceof operator cannot be used in a switch statement in Java.
---

**Contents**

[TOC]

### Answer
Yes, it is possible to use the instanceof operator in a switch statement in Java.

### Syntax
The syntax for using the instanceof operator in a switch statement is as follows:

```java
switch (expression) {
  case variable instanceof Type1:
    // Statements
    break;
  case variable instanceof Type2:
    // Statements
    break;
  // ...
  default:
    // Statements
}
```

### Example
For example, the following switch statement uses the instanceof operator to determine the type of a variable:

```java
Object obj = new Integer(10);

switch (obj) {
  case obj instanceof Integer:
    System.out.println("obj is an Integer");
    break;
  case obj instanceof String:
    System.out.println("obj is a String");
    break;
  default:
    System.out.println("obj is of unknown type");
}
```

In this example, the output will be `obj is an Integer`.
