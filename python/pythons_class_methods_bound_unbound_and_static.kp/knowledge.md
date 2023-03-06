---
title: Different types of class methods in Python bound, unbound, and static
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Bound methods receive an implicit first parameter which refers to the instance that the method is called upon, unbound methods do not have this parameter and therefore can be called without an instance, while static methods are simply functions defined inside a class that do not have access to class or instance variables.
---

**Contents**

[TOC]

# Introduction
Python allows the definition of three types of class methods, namely: bound, unbound, and static. In this article, we’ll take a closer look at each of these methods and their differences.

# Bound Methods
A bound method is a type of class method that is used when an instance of a class calls a method from its parent’s class. In other words, bound methods are instance-specific, and they require an instance to operate. A bound method is created when a method is called through an instance of the class. When this happens, the instance is passed as the first parameter to the function. The instance is then assigned to the first parameter in the method signature, which is usually called self.

# Unbound Methods
Unbound methods are similar to bound methods, but they do not require an instance of a class to operate. Instead, they are called directly on the class itself. It is the responsibility of the caller to provide an instance of the class when calling the method. Unlike bound methods, unbound methods do not have a self parameter in their signature.

# Static Methods
Unlike bound and unbound methods, static methods are not associated with the class or its instances. They are regular functions that are bound to the class simply because they are defined within the class scope. Static methods are defined using the @staticmethod decorator, and they do not take any specific parameters like self or cls.

# Conclusion
In conclusion, bound, unbound, and static methods in Python are used to provide unique methods of accessing class methods. Bound methods are instance-specific and require an instance to operate, unbound methods do not require an instance of a class to operate, and static methods are regular functions that are bound to the class simply because they are defined within the class scope. Understanding these differences is crucial in designing efficient and scalable Python applications.
