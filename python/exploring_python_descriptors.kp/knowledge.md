---
title: Grasping the concept of __get__ and __set__ and their use in Python descriptors
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Python descriptors are special methods used to define and manipulate the attributes of a class, such as \_\_get\_\_ and \_\_set\_\_, which are used to retrieve and set the values of an attribute, respectively.
---

**Contents**

[TOC]

#### What are Descriptors?
Descriptors are a type of object in Python that provides a way to customize attribute access. They are used to define properties of an object, and provide functionality when an attribute is accessed, set, or deleted. Descriptors are most commonly used to provide additional functionality to an object, such as implementing a custom getter and setter for an attribute.

#### What are __get__ and __set__?
The __get__ and __set__ methods are special methods that are part of the descriptor protocol. The __get__ method is called when an attribute is accessed, and allows for custom behavior when an attribute is accessed. The __set__ method is called when an attribute is set, and allows for custom behavior when an attribute is set. 

#### How to Use Descriptors
Descriptors can be used to create custom getters and setters for an attribute. To do this, the descriptor must be defined as a class, and the __get__ and __set__ methods must be implemented. The __get__ method should return the value of the attribute, and the __set__ method should set the value of the attribute. The descriptor can then be used to define a property on an object, and the custom getters and setters will be used when the attribute is accessed or set.

#### Benefits of Descriptors
Descriptors provide a way to customize attribute access and provide additional functionality when an attribute is accessed or set. This is especially useful for implementing custom getters and setters, as well as providing additional functionality when an attribute is accessed or set. Additionally, descriptors can be used to create properties on an object, which allows for more control over how an attribute is accessed and set.
