---
title: How does angularjs use prototypal / prototypical inheritance to define the scope of an object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: In AngularJS, prototypal inheritance allows objects to inherit directly from other objects, while prototypical inheritance allows objects to inherit from a prototype object.
---

**Contents**

[TOC]

## What is Prototypal Inheritance?
Prototypal inheritance is a type of inheritance in which an object is based on another object, and can access and inherit its properties and methods. In JavaScript, all objects have a prototype. This prototype can be accessed and modified to create new objects that inherit the properties and methods of the original object.

## How is it Used in AngularJS?
In AngularJS, prototypal inheritance is used to create directives and services. Directives are components that allow developers to extend HTML with custom attributes and elements. Services are custom objects that can be used to share data and logic across different parts of an application. Both directives and services use prototypal inheritance to define and extend their functionality.

## Benefits of Prototypal Inheritance
Prototypal inheritance offers a number of benefits for AngularJS developers. It allows developers to create reusable components that can be easily extended and modified. It also allows developers to create complex objects with minimal code, as they can inherit the properties and methods of existing objects.

## Drawbacks of Prototypal Inheritance
Although prototypal inheritance is a powerful tool, it can also be difficult to debug and maintain. When creating complex objects, it can be difficult to keep track of all the different objects and their properties. Additionally, it can be difficult to ensure that all objects are properly initialized and that all properties are set correctly.
