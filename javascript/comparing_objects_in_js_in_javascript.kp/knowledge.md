---
title: Comparing objects in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Object comparison in JavaScript can be done using the comparison operators (==, ===, !=, !==, etc.) or the Object.is() method.
---

**Contents**

[TOC]

### Primitive Types
For primitive types (`string`, `number`, `boolean`, `null`, `undefined`), comparison is done with the `===` operator. If two values are of the same type and have the same value, the `===` operator will return `true`.

### Reference Types
For reference types (`object`, `array`, `function`), comparison is done with the `==` operator. This operator will compare the references of the two values, not the values themselves. If the references point to the same object, the `==` operator will return `true`.

### Deep Comparison
For deep comparison, the `Object.is()` method can be used. This method will compare the values of two variables, even if the types are different. It will also consider `NaN` and `+0/-0` to be equal.

### Custom Comparison
For custom comparison, the `.equals()` method can be used. This method will compare two objects based on custom logic. It can be used to compare objects of different types, and can be used to compare objects with multiple properties.
