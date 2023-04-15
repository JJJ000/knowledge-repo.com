---
title: What is the distinction between an interface and an @interface in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: An interface is a type that defines a set of methods, while an @interface is a type that defines annotations.
---

**Contents**

[TOC]

### Interface
An interface in Java is a reference type, similar to a class, that can contain only constants, method signatures, and nested types. It is not possible to create an instance of an interface, nor can it contain any implementation of the methods. Interfaces are used to define a type, to specify the behavior of a class, and to declare methods that one or more classes must implement.

### @Interface
An @interface in Java is an annotation type. It is used to create custom annotations, which can be used to add information to a Java class, method, or field. The @interface annotation can contain elements such as default values, methods, and other annotations. It is also possible to use the @interface annotation to define an annotation type that can be used to annotate other elements.
