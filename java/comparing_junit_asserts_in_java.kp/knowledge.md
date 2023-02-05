---
title: What are the distinctions between the two junit assert classes?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The two JUnit Assert classes are Assert and AssertJ, which differ in that Assert is a legacy class with basic assertion methods, while AssertJ provides a more modern, fluent API with additional assertion methods.
---

**Contents**

[TOC]

**Assert.assertEquals()**
- Purpose: 
This method is used to compare two values to determine if they are equal.
- Syntax:
assertEquals(expected, actual)
- Parameters: 
expected: the expected value
actual: the actual value

**Assert.assertTrue()**
- Purpose: 
This method is used to check if a condition is true.
- Syntax:
assertTrue(condition)
- Parameters: 
condition: the condition to be checked
