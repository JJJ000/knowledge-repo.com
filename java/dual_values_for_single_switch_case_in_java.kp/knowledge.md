---
title: Creating a switch case statement with two different values
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is not possible to use two values for one switch case statement in Java.
---

**Contents**

[TOC]

### Overview
It is possible to use two values for one switch case statement in Java. This is done by using a combination of the switch statement and the logical OR operator (||). 

### Syntax
The syntax for using two values for one switch case statement in Java is as follows: 

```java
switch (expression) {
  case value1 || value2:
    // code to be executed
    break;
    .
    .
    .
}
```

### Example
For example, if you wanted to execute the same code for the values "red" and "blue", you could use the following switch statement:

```java
switch (color) {
  case "red" || "blue":
    System.out.println("The color is either red or blue.");
    break;
    .
    .
    .
}
```

### Considerations
It is important to note that when using two values for one switch case statement, the expression must be the same for both values. For example, the following statement would not be valid:

```java
switch (color) {
  case "red" || 3:
    System.out.println("The color is either red or 3.");
    break;
    .
    .
    .
}
```

In this case, the expression "color" is a String, while the second value is an integer. This is not allowed, as the expression must be the same for both values.
