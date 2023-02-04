---
title: What are the characteristics of a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can enumerate the properties of a JavaScript object by using the Object.keys() or Object.entries() methods.
---

**Contents**

[TOC]

1. **Using a `for...in` Loop**

A `for...in` loop is a simple way to enumerate the properties of a JavaScript object. It will iterate over all the enumerable properties of an object, and for each property, it will execute a block of code.

```js
let obj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
};

for (let property in obj) {
    console.log(property + ': ' + obj[property]);
}
```

2. **Using `Object.keys()`**

`Object.keys()` is a method that returns an array of the object's own enumerable properties. This can be used to iterate over an object's properties.

```js
let obj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
};

let properties = Object.keys(obj);

for (let i = 0; i < properties.length; i++) {
    console.log(properties[i] + ': ' + obj[properties[i]]);
}
```

3. **Using `Object.entries()`**

`Object.entries()` is a method that returns an array of the object's own enumerable property [key, value] pairs. This can be used to iterate over an object's properties.

```js
let obj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
};

let entries = Object.entries(obj);

for (let entry of entries) {
    console.log(entry[0] + ': ' + entry[1]);
}
```

4. **Using `Object.getOwnPropertyNames()`**

`Object.getOwnPropertyNames()` is a method that returns an array of the object's own properties (enumerable or not). This can be used to iterate over an object's properties.

```js
let obj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
};

let properties = Object.getOwnPropertyNames(obj);

for (let i = 0; i < properties.length; i++) {
    console.log(properties[i] + ': ' + obj[properties[i]]);
}
```
