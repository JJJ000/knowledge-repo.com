---
title: What contrasts a JavaBean from a pojo?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A JavaBean is a POJO with additional conventions for properties and getter/setter methods.
---

**Contents**

[TOC]

### Definition
A JavaBean is a reusable component based on the Java programming language that follows certain conventions for naming, fields, and methods. A POJO (Plain Old Java Object) is a Java object that does not follow any conventions or extend any special classes.

### Properties
A JavaBean must have a default constructor, getter and setter methods for each property, and private fields with public accessors. A POJO does not have any such requirements.

### Usage
A JavaBean is usually used to encapsulate data and provide a way to access and manipulate it. A POJO is typically used as a simple Java object to represent domain data and business logic.

### Framework Support
JavaBeans are supported by many frameworks, such as JavaServer Faces (JSF), JavaServer Pages (JSP), and Enterprise JavaBeans (EJB). POJOs are not supported by any frameworks.
