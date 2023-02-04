---
title: What are the distinctions between typeof and instanceof, and when should each be utilized instead of the other?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Typeof should be used to check the type of a variable, while instanceof should be used to check the type of an object`s prototype.
---

**Contents**

[TOC]

### Typeof

The typeof operator is used to check the type of a variable. It returns a string that indicates the type of the variable. It will return "object" for objects, "function" for functions, "string" for strings, and so on.

### Instanceof

The instanceof operator is used to check if an object is an instance of a particular constructor. It returns true if the object is an instance of the constructor and false if it is not.

### When to Use

Typeof should be used when you want to check the type of a variable. Instanceof should be used when you want to check if an object is an instance of a particular constructor. 

### Summary

In summary, typeof should be used to check the type of a variable, while instanceof should be used to check if an object is an instance of a particular constructor.
