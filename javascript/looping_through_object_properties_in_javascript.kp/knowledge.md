---
title: Loop over the properties of the object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To iterate through object properties in Javascript, you can use the for-in loop.
---

**Contents**

[TOC]

### For-in Loop

The most common way to iterate through object properties is to use a `for-in` loop. This loop allows us to loop through all of the enumerable properties of an object.

```javascript
const obj = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

for (let key in obj) {
  console.log(`${key}: ${obj[key]}`);
}
```

### Object.keys()

Another way to iterate through object properties is to use the `Object.keys()` method. This method returns an array of all the keys in the object.

```javascript
const obj = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

const keys = Object.keys(obj);

for (let i = 0; i < keys.length; i++) {
  console.log(`${keys[i]}: ${obj[keys[i]]}`);
}
```

### Object.entries()

The `Object.entries()` method can also be used to iterate through object properties. This method returns an array of arrays, where each array contains a key-value pair.

```javascript
const obj = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

const entries = Object.entries(obj);

for (let [key, value] of entries) {
  console.log(`${key}: ${value}`);
}
```

### Object.getOwnPropertyNames()

The `Object.getOwnPropertyNames()` method can be used to iterate through all of the properties of an object, including non-enumerable properties.

```javascript
const obj = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

const keys = Object.getOwnPropertyNames(obj);

for (let i = 0; i < keys.length; i++) {
  console.log(`${keys[i]}: ${obj[keys[i]]}`);
}
```
