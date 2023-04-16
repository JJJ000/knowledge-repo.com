---
title: What does 'null' mean in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Null in Java is a special value that indicates that a reference variable does not point to any object.
---

**Contents**

[TOC]

## Definition
Null is a special value in Java that indicates that no value has been assigned to a variable. It is denoted by the keyword `null`.

## Usage
Null is commonly used when a variable has not yet been assigned a value. For example, a variable of type `String` can be initialized to `null` if its value has not yet been set.

## Comparison
It is important to note that `null` is not the same as an empty string (`""`) or a zero value (`0`). An empty string is a valid value and indicates an empty string, while a zero value indicates a numerical value of zero.

## NullPointerException
In Java, when an operation is performed on a `null` value, a `NullPointerException` is thrown. This is because `null` does not refer to a valid object and therefore cannot be operated on.
