---
title: What are the benefits of using static methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Static methods should be used when a method needs to be accessed without creating an instance of the containing class.
---

**Contents**

[TOC]

1. **When to Use Static Methods**
Static methods are useful when a method does not need to access any instance variables of a class. They can also be used to create utility methods that can be used without creating an instance of the class.

2. **When Not to Use Static Methods**
Static methods should not be used when a method needs to access instance variables of a class, as this will lead to unexpected results. In addition, static methods should not be used when a method needs to be overridden, as this is not possible with static methods.

3. **Performance Benefits of Static Methods**
Static methods can improve performance, as they are loaded into memory only once when the class is loaded. This means that subsequent calls to the method can be made without having to reload the class.

4. **Limitations of Static Methods**
Static methods are limited in their scope, as they can only access static variables and cannot access instance variables. In addition, static methods cannot be overridden, so they cannot be changed or customized for different scenarios.
