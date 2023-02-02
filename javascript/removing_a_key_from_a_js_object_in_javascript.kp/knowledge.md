---
title: What is the best way to delete a key from a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the delete operator to remove a key from a JavaScript object.
---

**Contents**

[TOC]

1. Using the `delete` Keyword

The most straightforward way to remove a key from a JavaScript object is to use the `delete` keyword. This keyword will delete the specified property from the object.

```javascript
const myObject = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

delete myObject.key2;

console.log(myObject);
// Output: {key1: 'value1', key3: 'value3'}
```

2. Using the `Object.assign()` Method

Another way to remove a key from a JavaScript object is to use the `Object.assign()` method. This method creates a new object and copies the properties of the original object, excluding the specified property.

```javascript
const myObject = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

const newObject = Object.assign({}, myObject, { key2: undefined });

console.log(newObject);
// Output: {key1: 'value1', key3: 'value3'}
```

3. Using the `Object.keys()` and `Object.defineProperty()` Methods

The `Object.keys()` and `Object.defineProperty()` methods can also be used to remove a key from a JavaScript object. The `Object.keys()` method returns an array of the object's keys, which can then be used to loop through the keys and delete the specified property using the `Object.defineProperty()` method.

```javascript
const myObject = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

const keys = Object.keys(myObject);

for (let i = 0; i < keys.length; i++) {
  if (keys[i] === 'key2') {
    Object.defineProperty(myObject, keys[i], {
      value: undefined,
      enumerable: true,
      writable: true,
      configurable: true
    });
  }
}

console.log(myObject);
// Output: {key1: 'value1', key3: 'value3'}
```

4. Using the `Object.entries()` and `Object.fromEntries()` Methods

The `Object.entries()` and `Object.fromEntries()` methods can also be used to remove a key from a JavaScript object. The `Object.entries()` method returns an array of the object's key-value pairs, which can then be used to filter out the specified property using the `Array.filter()` method. The filtered array can then be converted back into an object using the `Object.fromEntries()` method.

```javascript
const myObject = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};

const entries = Object.entries(myObject);

const filteredEntries = entries.filter(([key]) => key !== 'key2');

const newObject = Object.fromEntries(filteredEntries);

console.log(newObject);
// Output: {key1: 'value1', key3: 'value3'}
```
