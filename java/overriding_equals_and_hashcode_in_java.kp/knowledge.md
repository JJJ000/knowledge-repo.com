---
title: What are the benefits of overriding the equals and hashcode methods in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To ensure that objects are compared and stored based on their logical equality rather than their reference equality.
---

**Contents**

[TOC]

### What are the equals and hashCode methods?
The equals and hashCode methods are two methods that are part of the Object class in Java. The equals method is used to compare two objects to see if they are equal, while the hashCode method is used to generate a numerical representation of an object.

### Why should they be overridden?
The equals and hashCode methods should be overridden when creating a new class because the default implementations are not always accurate. For example, the default implementation of the equals method only checks if two objects are the same instance, not if they have the same values. Similarly, the default implementation of the hashCode method does not always generate a unique numerical representation for each object.

### How to override the methods?
To override the equals and hashCode methods, you must first create a new class that extends the Object class. Then, you can override the methods by implementing the following code:

```java
@Override
public boolean equals(Object o) {
    // Your implementation here
}

@Override
public int hashCode() {
    // Your implementation here
}
```

### Benefits of overriding
By overriding the equals and hashCode methods, you can ensure that your objects are being compared and represented accurately. This can be beneficial in many situations, such as when using collections or when performing comparisons.
