---
title: What is the method for obtaining the distinct id of an object that has overridden hashcode()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Object`s hashCode() method to get the unique ID of an object which overrides hashCode().
---

**Contents**

[TOC]

# Section 1: Introduction

Objects in Java can override the hashCode() method to return a unique ID. This ID can be used to identify the object and can be used to compare the object with other objects in the same class.

# Section 2: How to Get the Unique ID

The unique ID of an object which overrides hashCode() can be obtained by calling the hashCode() method on the object. The returned value will be the unique ID of the object.

# Section 3: Example

For example, if we have an object of class Person which overrides the hashCode() method, we can get the unique ID of the object by calling the hashCode() method on it.

Person person = new Person(); 
int uniqueId = person.hashCode(); // uniqueId will be the unique ID of the Person object

# Section 4: Conclusion

In conclusion, the unique ID of an object which overrides hashCode() can be obtained by calling the hashCode() method on the object. This ID can be used to identify the object and can be used to compare the object with other objects in the same class.
