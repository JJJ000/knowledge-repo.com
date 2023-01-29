---
title: Utilizing "instanceof" in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: `instanceof` is an operator in Java used to check if an object is an instance of a specific class or an interface.
---

**Contents**

[TOC]

### What is "instanceof"

"instanceof" is an operator in the Java programming language that allows developers to check if an object belongs to a particular class or is an instance of that class.

### How "instanceof" is Used

The "instanceof" operator is used to check if an object is an instance of a class, an interface, or an array. It takes two operands, an object reference and a class, interface, or array type, and returns true if the object is an instance of the specified type.

### Example

For example, if we have a class called Animal and a class called Dog that extends Animal, we can use the "instanceof" operator to check if an object is an instance of the class Dog:

```java
Animal animal = new Dog();
if (animal instanceof Dog) {
  System.out.println("animal is an instance of Dog");
}
```

### Advantages

Using the "instanceof" operator allows developers to quickly and easily check if an object is an instance of a particular type, which can be useful for validating user input or for creating more efficient and robust code.
