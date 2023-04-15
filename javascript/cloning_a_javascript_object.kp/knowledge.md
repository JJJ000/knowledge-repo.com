---
title: What is the proper way to clone a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the Object.assign() or spread operator (...) to create a shallow clone of the object.
---

**Contents**

[TOC]

### Shallow Cloning
A shallow clone of an object can be created by using the `Object.assign()` method. This method will copy the values of all enumerable own properties from one or more source objects to a target object.

### Deep Cloning
A deep clone of an object can be created by using the `JSON.parse(JSON.stringify(obj))` method. This method will take a JavaScript object and create a deep clone of it by converting the object into a JSON string, and then parsing the JSON string back into an object.

### Deep Cloning with Circular References
When cloning an object that contains circular references, the `JSON.parse(JSON.stringify(obj))` method will not work. In order to clone an object with circular references, a custom deep cloning function must be used.

### Custom Deep Cloning Function
A custom deep cloning function can be used to clone an object that contains circular references. This function should traverse the object and clone each property, checking for any circular references along the way. If a circular reference is found, the function should store a reference to the object instead of cloning it.
