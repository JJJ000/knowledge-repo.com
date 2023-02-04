---
title: What is the distinction between null and undefined in javascript, and how do == and === differ?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Null is a value that means `no value`, while undefined means that a variable has been declared but has not been assigned a value; == checks for equality of value, while === checks for equality of both value and type.
---

**Contents**

[TOC]

## Checking for Null vs. Undefined

In JavaScript, both `null` and `undefined` represent empty values. However, they are two distinct types of values. `Undefined` is used to indicate that a variable has been declared but has not been assigned a value. On the other hand, `null` is an assignment value that indicates that an object has no value.

## Difference between == and ===

The difference between `==` and `===` is that `==` is a loose comparison operator, while `===` is a strict comparison operator. The `==` operator will compare two values after converting them to a common type, while the `===` operator will only compare two values if they are of the same type.
