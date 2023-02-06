---
title: The distinction between inheritance and composition is that inheritance involves a class receiving methods and fields from a parent class, while composition involves an object containing a reference to another object or objects which it relies on to function
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Inheritance is a relationship between two classes where one class inherits the properties of another, whereas Composition is a relationship between two classes where one class contains the other class as a member.
---

**Contents**

[TOC]

#### Inheritance
Inheritance is a mechanism in Java by which one class can acquire the properties and behavior of another. It is a way to reuse code of existing object. Inheritance enables us to define a class in terms of another class, which makes it easier to create and maintain an application.

#### Composition
Composition is a way to combine objects and classes into larger structures. It is a special type of aggregation wherein one class contains a reference to another class. Composition is a structural relationship that represents part-of relationship. Unlike inheritance, composition is a design choice that models a has-a relationship.

#### Difference
- Inheritance is a unidirectional relationship between two classes, whereas composition is a bidirectional relationship between two classes.
- Inheritance allows subclasses to access the public and protected members of the superclass, whereas composition does not allow this.
- Inheritance is more like an 'is-a' relationship, whereas composition is like a 'has-a' relationship.
- Inheritance is more suitable for the situation when a class is a specialization of another class, whereas composition is suitable for the situation when a class has a collection of objects of other classes.
