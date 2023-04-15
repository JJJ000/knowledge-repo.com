---
title: What are the potential issues with using an overridable method in a constructor?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Calling an overridable method in a constructor can lead to unexpected behavior if the subclass overrides the method.
---

**Contents**

[TOC]

### Violation of Principle of Least Astonishment
The Principle of Least Astonishment states that a system should behave in a way that minimizes the user's surprise. When a method is called from a constructor, the behavior may be unexpected because the constructor is usually used to set up the state of the object and the method is expected to modify the state of the object. This can lead to unexpected behavior and surprise the user.

### Violation of Encapsulation
When a method is called from a constructor, it violates the principle of encapsulation. The constructor should only be responsible for setting up the state of the object and any modifications should be done through methods. By calling a method from the constructor, the object's state is being modified without using the appropriate methods, which can lead to unexpected behavior.

### Violation of Separation of Concerns
When a method is called from a constructor, it violates the principle of separation of concerns. The constructor should only be responsible for setting up the state of the object and any modifications should be done through methods. By calling a method from the constructor, the object's state is being modified without using the appropriate methods, which can lead to unexpected behavior.

### Violation of DRY Principle
The DRY (Don't Repeat Yourself) principle states that code should not be repeated unnecessarily. When a method is called from a constructor, it violates this principle because the same code is being repeated in two different places. This can lead to errors and inconsistencies in the code.
