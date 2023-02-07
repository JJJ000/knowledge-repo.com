---
title: Comparing the usage of 'tobe' and 'toequal' in jasmine JavaScript testing
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: `toBe` checks for strict equality (same value and type), while `toEqual` checks for loose equality (same value).
---

**Contents**

[TOC]

1. **What is toBe?**

toBe is a matcher in Jasmine that is used to test for strict equality between two values. It uses the JavaScript === operator to compare two values and returns true if the values are strictly equal.

2. **What is toEqual?**

toEqual is a matcher in Jasmine that is used to test for deep equality between two objects. It uses the JavaScript Object.is() method to compare two objects and returns true if the objects are deeply equal.

3. **Difference between toBe and toEqual**

The main difference between toBe and toEqual is that toBe tests for strict equality between two values, while toEqual tests for deep equality between two objects. Strict equality means that the two values must be of the same type and have the same value, while deep equality means that the two objects must have the same properties and values.

4. **When to Use toBe and toEqual**

toBe should be used when testing for strict equality between two values, while toEqual should be used when testing for deep equality between two objects.
