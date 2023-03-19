---
title: Can you explain the distinction between class and instance attributes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Class attributes are shared by all instances of a class, while instance attributes are unique to each instance.
---

**Contents**

[TOC]

Class Attributes vs. Instance Attributes in Python

Introduction
In Python, both classes and instances are objects, and both can have attributes. However, there are some fundamental differences between class and instance attributes.

Definition
Class Attributes are variables that are shared among all instances of a class. They are defined within the class scope but outside of any methods. Instance Attributes are variables that are unique to each instance of a class. They are defined within a method, with "self" as the first parameter.

Scope
Class Attributes have a global scope within the class, meaning that they can be accessed by any method within the class. Instance Attributes have a local scope within the class, meaning that they can only be accessed by methods within the instance.

Memory Allocation
Class Attributes are stored in memory only once, regardless of the number of instances created. Instance Attributes are stored separately in memory for each instance created.

Accessibility
Class Attributes can be accessed and changed by both the class and its instances. Instance Attributes can only be accessed and changed by its instance.

Conclusion
In summary, Class Attributes are shared by all instances of a class, stored in memory only once, and can be accessed and changed by both the class and its instances. Instance Attributes are unique to each instance, stored separately in memory for each instance, and can only be accessed and changed by its instance. Understanding the difference between these attributes is crucial while working with Python classes.
