---
title: What is the difference between using `==` and `equals()` when comparing Java enum members?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: The `==` operator should be used to compare enum members, not the `equals()` method.
---

**Contents**

[TOC]

### "==" Operator
The `==` operator can be used to compare two enum members in Java. This operator checks if the two references refer to the same object. It will return `true` if the two objects are the same and `false` if they are not.

### equals()
The `equals()` method can also be used to compare two enum members in Java. This method checks if the two objects have the same value. It will return `true` if the two objects have the same value, and `false` if they do not.
