---
title: What is the difference between parseint() and valueof() in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: parseInt() returns the primitive int value of a string, while valueOf() returns the Integer object of a string.
---

**Contents**

[TOC]

### ParseInt()
- `parseInt()` is a static method of Java `Integer` class that is used to get the primitive data type of a certain String.
- It takes in a String as a parameter and returns the int representation of the String.
- It throws a `NumberFormatException` if the String does not contain a parsable integer.

### ValueOf()
- `valueOf()` is a static method of Java `Integer` class that is used to get the wrapper class of a certain String.
- It takes in a String as a parameter and returns the `Integer` class representation of the String.
- It throws a `NumberFormatException` if the String does not contain a parsable integer.
