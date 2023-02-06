---
title: Is the use of getters and setters considered bad design? there appears to be conflicting opinions on the matter
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, getters and setters are not necessarily poor design; however, there is some debate about when and how they should be used in Java.
---

**Contents**

[TOC]

## Overview

Getters and setters are methods used to access and modify the values of object properties. In object-oriented programming, they are commonly used to encapsulate the data within an object. While getters and setters are often seen as a necessary part of object-oriented programming, some argue that they are bad design and should be avoided.

## Arguments in Favor of Getters and Setters

Proponents of getters and setters argue that they provide an effective way to encapsulate data within an object. By using getters and setters, developers can control how data is accessed and modified, ensuring that data is not changed in unexpected ways. Additionally, getters and setters can be used to add validation logic or perform other tasks when data is accessed or modified.

## Arguments Against Getters and Setters

Critics of getters and setters argue that they can lead to code bloat and can make code more difficult to read and debug. Additionally, the use of getters and setters can lead to code that is tightly coupled, making it more difficult to refactor or modify.

## Contradictory Advice in Java

The advice on getters and setters in Java is somewhat contradictory. On the one hand, the JavaBeans standard encourages the use of getters and setters, and many Java frameworks rely on them. On the other hand, some Java developers argue that getters and setters should be avoided in favor of other approaches, such as using public fields or using the Builder pattern.
