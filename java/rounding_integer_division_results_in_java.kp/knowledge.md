---
title: What is the process for rounding the answer of an integer division?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Math.ceil() method to round up the result of integer division in Java.
---

**Contents**

[TOC]

#Using Math.ceil() 

####Syntax

`Math.ceil(double a)`

####Description

This method returns the smallest (closest to negative infinity) double value that is greater than or equal to the argument and is equal to a mathematical integer.

####Example

```java
int a = 5;
int b = 2;

System.out.println(Math.ceil(a/b));
```

Output:
`3.0`
