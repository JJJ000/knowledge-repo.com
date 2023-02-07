---
title: Constructing an object with variable keys
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Objects can be created with dynamic keys in Javascript by using the bracket notation, such as object[key] = value.
---

**Contents**

[TOC]

##### Using ES6

ES6 introduces the ability to create objects with dynamic keys using the new [Computed Property Names](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#Computed_property_names).

```javascript
let key = 'keyName';
let obj = {
    [key]: 'value'
};
```

##### Using ES5

In ES5, we can use the `Object.defineProperty()` method to create objects with dynamic keys.

```javascript
let key = 'keyName';
let obj = {};
Object.defineProperty(obj, key, {
    value: 'value',
    writable: true,
    enumerable: true,
    configurable: true
});
```

##### Using Object Literals

We can also use object literals to create objects with dynamic keys.

```javascript
let key = 'keyName';
let obj = {
    [key]: 'value'
};
```
