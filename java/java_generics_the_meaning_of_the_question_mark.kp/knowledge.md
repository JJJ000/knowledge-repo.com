---
title: What is the significance of the question mark in Java generic type parameters?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The question mark in Java generics` type parameter is a wildcard character that represents an unknown type.
---

**Contents**

[TOC]

# What is a Type Parameter?
A type parameter is a special kind of parameter used in generic classes and methods. It is used to represent a type that will be specified when the class or method is used.

# What Does the Question Mark Mean?
The question mark in Java generics' type parameter indicates a wildcard. A wildcard is a special type of parameter that can represent any type. It can be used in place of a specific type when the exact type is not known or when a specific type is not needed. For example, a method that takes a List of objects can be written with a wildcard to indicate that any type of object can be passed in.
