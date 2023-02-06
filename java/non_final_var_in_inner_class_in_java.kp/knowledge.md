---
title: It is not possible to access a non-final variable from within an inner class that is defined in a different method
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, it is not possible to refer to a non-final variable inside an inner class defined in a different method in Java.
---

**Contents**

[TOC]

## Definition

In Java, an inner class is a class that is defined within another class. An inner class has access to the members of the class in which it is defined.

## Non-Final Variable

A non-final variable is a variable that is not declared as "final". It is possible to change the value of this variable at any time.

## Inner Class in Different Method

When an inner class is defined in a different method than the one in which it is used, the inner class does not have access to the non-final variables that are declared in the method in which it is defined.

## Solution

The only way to refer to a non-final variable inside an inner class defined in a different method is to declare the variable as "final". This ensures that the variable cannot be changed and that the inner class will have access to it.
