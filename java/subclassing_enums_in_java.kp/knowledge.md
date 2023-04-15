---
title: Is it possible to create a subclass of an enum to add new elements?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, enums cannot be subclassed in Java.
---

**Contents**

[TOC]

### Yes
Enums can be subclassed to add new elements in Java. This is done by creating a new class that extends the existing enum class. The new class should have a constructor that takes in the enum values and adds any new elements.

### Example
For example, consider the following enum class:

```java
public enum Colors {
    RED,
    GREEN,
    BLUE
}
```

To add a new element to this enum, a new class can be created that extends the Colors enum:

```java
public class ExtendedColors extends Colors {
    YELLOW
}
```

The constructor for the new class should take in the existing enum values and add the new element:

```java
public ExtendedColors() {
    super(RED, GREEN, BLUE);
    this.YELLOW = new ExtendedColors("YELLOW");
}
```

### Benefits
Subclassing enums provides a number of benefits. It allows for the addition of new elements without breaking existing code, and it also allows for the creation of more complex data structures with the enum values. Additionally, subclassing enums makes it easier to maintain code consistency and enforce rules around enum values.
