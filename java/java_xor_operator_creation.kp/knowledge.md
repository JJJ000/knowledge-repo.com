---
title: Constructing a Java operator for "logical exclusive or"
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The logical exclusive or operator in Java can be created by using the bitwise XOR operator (^).
---

**Contents**

[TOC]

**Section 1 - Definition**

A logical exclusive or (XOR) operator is a logical operator that returns a true value if and only if one, and only one, of its operands is true. 

**Section 2 - Syntax**

In Java, the syntax for a logical XOR operator is `^`. 

**Section 3 - Example**

For example, the following expression would evaluate to true: 

`(true ^ false) == true`

**Section 4 - Usage**

The logical XOR operator is useful for cases where only one of two conditions can be true. For example, it can be used to check if a number is odd or even: 

`(n % 2 == 0) ^ (n % 2 != 0)`
