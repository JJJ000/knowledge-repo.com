---
title: What is the purpose of the "final" keyword in Java and can I still modify an object after it has been declared final?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `final` keyword in Java prevents the object from being reassigned to a different object, but it does not prevent the object`s contents from being modified.
---

**Contents**

[TOC]

### Definition
The "final" keyword in Java is used to indicate that a variable is a constant, meaning that its value cannot be changed. It is also used to indicate that a method cannot be overridden, and that a class cannot be extended.

### Modifying Objects
Even though a variable is declared as "final", the object it references can still be modified. For example, if a "final" variable is declared as a list, the contents of the list can still be changed.

### Benefits
Using the "final" keyword has two major benefits. First, it helps to prevent accidental changes to a variable's value. Second, it can improve code readability, as it is immediately obvious that the value of a "final" variable will not change.

### Limitations
The "final" keyword does have some limitations. It can only be used with primitive data types, such as int or double, and not with objects. Additionally, it cannot be used to prevent a method from being overridden in a subclass, as this is only possible with the "final" keyword applied to the class itself.
