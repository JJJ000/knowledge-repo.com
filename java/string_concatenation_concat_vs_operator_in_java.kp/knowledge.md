---
title: Comparing the methods of combining strings the concat() function versus the '+' symbol
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `+` operator is faster and more concise than the concat() method, but concat() is more flexible.
---

**Contents**

[TOC]

**Concat() Method**
- The `concat()` method is a static method of the `String` class. It is used to join two or more strings together. 
- It is used to append one string to the end of another string. 
- The `concat()` method does not modify the existing strings, but instead returns a new string.

**+ Operator**
- The `+` operator is also used to join two or more strings together. 
- Unlike the `concat()` method, the `+` operator modifies the existing strings and doesn't return a new string. 
- The `+` operator is also used to add numerical values together, while the `concat()` method only works with strings.
