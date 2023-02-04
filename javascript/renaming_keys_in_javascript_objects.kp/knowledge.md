---
title: Renaming a key in a JavaScript object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: In JavaScript, an object key can be renamed using the bracket notation and the assignment operator.
---

**Contents**

[TOC]

## Using ES6
ES6 (ECMAScript 6) introduced the [`Object.defineProperty()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty) method, which allows us to define a new property on an object, or modify an existing one.

```javascript
let obj = {
  oldKey: 'value'
};

Object.defineProperty(obj, 'newKey', {
  value: obj.oldKey,
  writable: true,
  enumerable: true,
  configurable: true
});

delete obj.oldKey;

console.log(obj); // { newKey: 'value' }
```

## Using Lodash
The [`lodash.set()`](https://lodash.com/docs/4.17.15#set) method can be used to rename a key in an object.

```javascript
let obj = {
  oldKey: 'value'
};

_.set(obj, 'newKey', _.get(obj, 'oldKey'));
delete obj.oldKey;

console.log(obj); // { newKey: 'value' }
```

## Using a for-loop
We can also use a for-loop to iterate over the object and rename the key.

```javascript
let obj = {
  oldKey: 'value'
};

for (let key in obj) {
  if (key === 'oldKey') {
    obj['newKey'] = obj[key];
    delete obj[key];
  }
}

console.log(obj); // { newKey: 'value' }
```
