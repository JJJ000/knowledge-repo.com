---
title: What are the characteristics of a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The properties of a JavaScript object can be listed using the Object.keys() or Object.getOwnPropertyNames() methods.
---

**Contents**

[TOC]

1. **Using `Object.keys()`**

Object.keys() is a method that returns an array of a given object's own enumerable property names.

```javascript
Object.keys(obj);
```

2. **Using `for...in` loop**

The `for...in` loop iterates over all non-Symbol, enumerable properties of an object.

```javascript
for (var key in obj) {
  console.log(key);
}
```

3. **Using `Object.getOwnPropertyNames()`**

Object.getOwnPropertyNames() returns an array of all properties (enumerable or not) found directly upon a given object.

```javascript
Object.getOwnPropertyNames(obj);
```

4. **Using `Object.entries()`**

Object.entries() returns an array of a given object's own enumerable string-keyed property [key, value] pairs.

```javascript
Object.entries(obj);
```
