---
title: What is the difference between the '==' and '===' operators when making comparisons in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The triple equals operator (===) should be used in JavaScript comparisons as it checks for both value and type.
---

**Contents**

[TOC]

**== Operator**

The == operator is used to compare two values for equality. It will attempt to convert the values to the same type before performing the comparison.

**=== Operator**

The === operator is used to compare two values for strict equality. It does not attempt to convert the values to the same type before performing the comparison.

**Which to Use**

The === operator should be used in most cases as it provides more accurate results. The == operator can lead to unexpected results due to type conversion.
