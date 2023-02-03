---
title: What is the cause of the strange JavaScript behaviors discussed in the 'wat' presentation at codemash 2012?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The bizarre behaviours mentioned in the `Wat` talk are caused by JavaScript`s implicit type coercion, which can lead to unexpected results when working with variables of different types.
---

**Contents**

[TOC]

## Primitive Types

In JavaScript, primitive types are immutable, meaning that operations on them will not change their value. This means that when a primitive type is passed as an argument to a function, a copy of that value is made, and the original value remains unchanged.

## Reference Types

Reference types, on the other hand, are mutable. This means that when they are passed as arguments to a function, the original value is modified. This can lead to unexpected behaviour, as the original value is changed without the programmer's knowledge.

## Equality

In JavaScript, the equality operator (`==`) does not compare the values of two objects, but instead compares their references. This means that two objects are considered equal even if they have different values.

## Automatic Type Conversion

In JavaScript, the language will automatically convert one type to another when necessary. This can lead to unexpected behaviour when comparing values of different types, as the values may be converted before the comparison is made.
