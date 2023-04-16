---
title: What are the differences between lodash's .extend(), .assign(), and .merge() functions?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: .extend() / .assign() will overwrite properties of the same name, while .merge() will combine properties of the same name.
---

**Contents**

[TOC]

**.extend() / .assign()**

- Definition: The `.extend()` and `.assign()` methods are used to copy the values of all enumerable own properties from one or more source objects to a target object.

- Syntax: `Object.assign(target, ...sources)`

- Usage: `Object.assign()` is used to copy the values of all enumerable own properties from one or more source objects to a target object. It will return the target object.

- Difference from `.merge()`: `.extend()` and `.assign()` are shallow copies, which means that they copy the values of the properties, but not the properties themselves. 

**.merge()**

- Definition: The `.merge()` method is used to merge the source object(s) into the target object, recursively merging object properties and arrays.

- Syntax: `_.merge(object, [sources])`

- Usage: `_.merge()` is used to merge the source object(s) into the target object, recursively merging object properties and arrays. It will return the target object.

- Difference from `.extend()` / `.assign()`: `.merge()` is a deep copy, which means that it will copy the properties and their values, including any nested objects or arrays.
