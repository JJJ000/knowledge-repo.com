---
title: The unchangeability of strings in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Strings in Java are immutable, meaning their values cannot be changed once created.
---

**Contents**

[TOC]

### What is Immutability?
Immutability is a programming concept that refers to an object's inability to be modified after it has been created. In other words, an immutable object cannot be changed once it has been instantiated.

### Strings in Java
In Java, Strings are immutable objects. This means that once a String object has been created, its value cannot be changed. Any operation that attempts to modify a String object will result in a new String object being created.

### Benefits of Immutability
The immutability of Strings in Java provides several benefits. It ensures that the value of a String object is always consistent and can’t be changed unexpectedly, making it easier to reason about code. It also improves the performance of applications because Strings can be cached and reused without having to worry about them being modified.

### Conclusion
In conclusion, Strings in Java are immutable objects, meaning that their values cannot be changed once they have been created. This immutability provides several benefits, including improved code readability and performance.
