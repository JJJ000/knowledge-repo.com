---
title: How does a Python "property" differ from an "attribute"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: An attribute is a value stored in an object, while a property is a method that can be used to retrieve or set the value of an attribute.
---

**Contents**

[TOC]

## Introduction
Python is an object-oriented programming language that treats everything as an object. An object comprises of attributes and methods that define its characteristics and behavior, respectively. In Python, attributes are used to store data, whereas methods are used to perform actions on the data. Python allows creating objects with dynamic attributes, which can be added or removed at runtime. This flexibility makes Python a popular choice in software development. 

## Attributes 
In Python, an attribute is a variable that is associated with an object. It can be a data member or a method of an object. Every object in Python has its attributes, which can be accessed using the dot (.) operator. Attributes can be classified into two categories: class and instance attributes. 

### Class Attributes
A class attribute is a variable or a method that is common to all objects of a class. When any object of a class accesses a class attribute, it uses the same instance of the attribute that is shared among all objects of the class. They are defined within the class and outside of any method.

### Instance Attributes
Instance attributes are the unique attributes that belong to an instance of a class. It means that every object has its own distinct set of instance attributes. Instance attributes are created and initialized when an object is created.

## Properties
Properties, like attributes, are associated with objects in Python. However, properties are much more powerful than attributes since they provide a way to customize the access to an object's attributes. A property is a combination of two methods: getter and setter. A getter method returns the value of a property, whereas a setter method sets the value of a property. 

### Getter Method
A getter method is responsible for reading and returning the value of the property. It is typically named after the property it gets, with the prefix "get".

### Setter Method
A setter method is responsible for updating the value of the property. It is typically named after the property it sets, with the prefix "set".

## Differences Between Properties and Attributes
There are several differences between properties and attributes in Python:

1. Properties allow for customized access to the attribute's underlying data by providing a mechanism for validating, calculating, and modifying data during retrieval or assignment. Attributes simply store data.

2. Properties provide a level of abstraction, shielding the consumer of an object from implementation details. Attributes, on the other hand, are implementation details that can be accessed directly.

3. Properties are accessed using the same syntax as attributes in Python, using the dot notation. However, internally, property methods are invoked to retrieve or set the property value. 

## Conclusion
Python properties and attributes are both used to associate variables or methods with an object. The primary difference between the two is that properties provide a way to customize the retrieval and assignment of values stored in an object's attributes. Instances attributes, however, are more straightforward and simpler to use. Choosing between properties and attributes depends on the specific needs of an application.
