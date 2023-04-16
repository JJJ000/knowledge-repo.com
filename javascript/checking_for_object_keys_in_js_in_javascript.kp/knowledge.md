---
title: What is the process for determining if an object contains a specific key in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `in` operator to check if an object has a key.
---

**Contents**

[TOC]

1. Using `Object.prototype.hasOwnProperty()`

The `Object.prototype.hasOwnProperty()` method can be used to determine if an object has a specified property as a direct property of that object. 

```
const object = {
  key1: "value1",
  key2: "value2"
};

object.hasOwnProperty("key1"); // returns true
object.hasOwnProperty("key3"); // returns false
```

2. Using `in` operator

The `in` operator can be used to determine if an object has a specified property. It will return true if the property is present in the object, even if it is inherited from a prototype.

```
const object = {
  key1: "value1",
  key2: "value2"
};

"key1" in object; // returns true
"key3" in object; // returns false
```

3. Using `Object.keys()`

The `Object.keys()` method can be used to get an array of the properties of an object. This array can then be used to check if the object has a specified property.

```
const object = {
  key1: "value1",
  key2: "value2"
};

Object.keys(object).includes("key1"); // returns true
Object.keys(object).includes("key3"); // returns false
```

4. Using `Object.getOwnPropertyNames()`

The `Object.getOwnPropertyNames()` method can be used to get an array of the own properties of an object. This array can then be used to check if the object has a specified property.

```
const object = {
  key1: "value1",
  key2: "value2"
};

Object.getOwnPropertyNames(object).includes("key1"); // returns true
Object.getOwnPropertyNames(object).includes("key3"); // returns false
```
