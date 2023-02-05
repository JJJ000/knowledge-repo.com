---
title: Which method from the two interfaces is overridden when both are implemented in the same class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The method in the class will override the method from the interface that is implemented last.
---

**Contents**

[TOC]

**Section 1: What Happens When Two Interfaces Have the Same Method Name?**

When a class implements two interfaces that have the same method name, the class must override the method in order to resolve the conflict. The overridden method will be used when the class is instantiated.

**Section 2: What is Overriding?**

Overriding is a feature of object-oriented programming languages that allows a subclass or child class to provide a specific implementation of a method that is already provided by one of its superclasses or parent classes. When a method is overridden, the method of the subclass or child class will be used instead of the method of the superclass or parent class.

**Section 3: What is the Syntax for Overriding a Method?**

The syntax for overriding a method in Java is as follows:

```java
public class MyClass {
    // existing method
    public void doSomething() {
        // existing code
    }

    // overridden method
    @Override
    public void doSomething() {
        // new code
    }
}
```

**Section 4: What is the Benefit of Overriding a Method?**

The benefit of overriding a method is that it allows a subclass or child class to customize the behavior of a method that is inherited from a superclass or parent class. This allows for greater flexibility and code reuse.
