---
title: A Java method that has a declared return type will compile even if no return statement is included
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, a Java method with a return type can compile without a return statement, but it will always return the default value for the return type.
---

**Contents**

[TOC]

## Yes

A Java method with a return type can compile without a return statement. This is because the Java compiler will not throw an error if the return type is not explicitly specified. Instead, the compiler will assume the return type is `void`, meaning that the method does not return any value.

## No

However, if a return type is specified, the method must include a return statement. If a return type is specified and no return statement is included, the compiler will throw an error. This is because the compiler requires that a method with a specified return type must return a value of the same type.
