---
title: The difference between a private final static attribute and a private final attribute is that the static attribute is shared among all instances of the class, while the final attribute is specific to each instance
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A private final static attribute is a constant shared by all instances of a class, while a private final attribute is a constant unique to each instance of a class.
---

**Contents**

[TOC]

### Private Final Static Attribute
A private final static attribute is a variable that is declared as both private and static, and also as final. This means that the variable can only be accessed within the class it is declared in and cannot be changed. It is a constant that is shared among all instances of the class.

### Private Final Attribute
A private final attribute is a variable that is declared as both private and final. This means that the variable can only be accessed within the class it is declared in, and cannot be changed. However, unlike a private final static attribute, this variable is not shared among all instances of the class. Each instance of the class will have its own unique value for the variable.
