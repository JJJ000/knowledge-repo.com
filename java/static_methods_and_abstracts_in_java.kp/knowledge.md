---
title: What is the reason that static methods cannot be designated as abstract in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Static methods cannot be abstract in Java because they are associated with a class, not an instance of a class.
---

**Contents**

[TOC]

### Reason

Static methods cannot be abstract because abstract methods must be implemented by a subclass, but static methods are not associated with any particular instance of a class, and therefore cannot be overridden.

### Static Methods

Static methods are methods that are associated with the class, rather than any specific instance of that class. They are called "static" because they don't depend on the state of an object, and they can be called without creating an instance of the class.

### Abstract Methods

Abstract methods are methods that are declared, but not implemented in the class. Abstract methods must be implemented by any subclass that inherits from the parent class. This allows subclasses to define their own implementation of the method.

### Incompatible Features

Since static methods are not associated with any particular instance of a class, they cannot be overridden by subclasses. Therefore, it is not possible for a static method to be abstract, since abstract methods must be implemented by a subclass.
