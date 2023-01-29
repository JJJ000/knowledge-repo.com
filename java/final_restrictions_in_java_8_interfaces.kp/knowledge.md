---
title: What is the reason that Java 8 does not permit the use of the 'final' keyword in interface methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Final methods cannot be overridden in subclasses, which conflicts with the purpose of an interface.
---

**Contents**

[TOC]

### Explanation
Interfaces in Java 8 are allowed to contain default methods, which are methods with implementations. Since a final method cannot be overridden, it would be incompatible with the concept of default methods, and therefore is not allowed.

### Benefits of Default Methods
Default methods are beneficial because they allow existing interfaces to be extended without breaking existing implementations of those interfaces. This is especially useful when adding functionality to existing interfaces, as it allows new code to be written without having to modify existing code.

### Drawbacks of Final Methods
Final methods are inflexible, as they cannot be overridden. This means that any code that relies on the method being overridden will not work as expected. Additionally, final methods can lead to code that is difficult to maintain, as any changes to the method must be made in the original code, rather than in a subclass.

### Conclusion
In conclusion, final methods are not allowed in Java 8 interfaces because they are incompatible with the concept of default methods. Default methods are beneficial because they allow existing interfaces to be extended without breaking existing implementations, while final methods can lead to inflexible and difficult to maintain code.
