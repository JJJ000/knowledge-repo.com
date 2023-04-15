---
title: Comparing strings with the 'equals' method versus using the '==' operator
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: String.equals is used to compare the values of two strings, while `==` is used to compare two object references to see if they are referring to the same object.
---

**Contents**

[TOC]

### String.equals

`String.equals()` is a method used to compare two strings. It returns true if the strings are equal and false if they are not. This method is case sensitive and will return false if the strings have different cases.

### ==

`==` is an operator used to compare two values. It returns true if the values are equal and false if they are not. This operator is not case sensitive and will return true if the values have different cases.
