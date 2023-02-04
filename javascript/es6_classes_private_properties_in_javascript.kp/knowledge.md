---
title: Properties of JavaScript es6 classes that are not accessible outside the class
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Private properties in JavaScript ES6 classes can be declared using the `#` symbol before the property name.
---

**Contents**

[TOC]

#### Access Modifiers

Private properties in JavaScript ES6 classes are declared using the `#` symbol before the property name. This is known as the "hash syntax" and is used to indicate that the property is private.

#### Getters and Setters

Private properties can be accessed and modified using getters and setters. Getters are used to retrieve the value of a private property and setters are used to set the value of a private property.

#### Advantages

Private properties provide a way to control access to data and ensure that data is not accidentally modified or accessed by other parts of the code. This helps to ensure that the data is secure and that the code is more maintainable.

#### Disadvantages

The main disadvantage of using private properties is that they can be difficult to debug and maintain. Since the code is hidden from view, it can be difficult to determine what the code is doing and why it is not working as expected.
