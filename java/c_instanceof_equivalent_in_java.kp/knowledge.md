---
title: C++ equivalent of java's "is a" operator
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The C++ equivalent of java`s instanceof is the dynamic\_cast operator.
---

**Contents**

[TOC]

**1. dynamic_cast:**

Dynamic_cast is the C++ equivalent of Java's instanceof operator. It is used to check the type of an object at runtime. It takes a pointer or reference to a base class and casts it to a pointer or reference to a derived class. If the object is not of the derived class, then the cast returns a null pointer or reference.

**2. typeid:**

Typeid is a type-identification operator in C++. It is used to determine the type of an object at runtime. It takes an expression as an argument, and returns a reference to a const type_info object, which contains information about the type of the expression.

**3. RTTI (Run-Time Type Information):**

RTTI is a feature of the C++ language that enables a program to determine the type of an object at runtime. It is used in conjunction with typeid and dynamic_cast to identify the type of an object. It provides a set of functions and classes that allow a program to query the type of an object at runtime.

**4. std::is_base_of:**

std::is_base_of is a type trait that is used to determine whether one type is a base class of another type. It takes two types as template arguments and returns a boolean value that indicates whether the first type is a base class of the second type. It can be used in combination with typeid and dynamic_cast to identify the type of an object.
