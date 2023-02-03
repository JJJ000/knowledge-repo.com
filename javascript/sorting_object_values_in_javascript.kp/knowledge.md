---
title: Organizing object property according to values
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the Object.keys() and Array.sort() methods to sort an object`s properties by their values.
---

**Contents**

[TOC]

**Using the Object.entries() Method**

1. Extract the entries of the object using the Object.entries() method.

```javascript
const object = {
  a: 'one',
  b: 'two',
  c: 'three'
};

const entries = Object.entries(object);
console.log(entries);
// [['a', 'one'], ['b', 'two'], ['c', 'three']]
```

2. Sort the entries by their values using the Array.sort() method.

```javascript
const sortedEntries = entries.sort(([, valueA], [, valueB]) => {
  if (valueA < valueB) {
    return -1;
  }
  if (valueA > valueB) {
    return 1;
  }
  return 0;
});
console.log(sortedEntries);
// [['a', 'one'], ['b', 'two'], ['c', 'three']]
```

3. Create a new object from the sorted entries using the Object.fromEntries() method.

```javascript
const sortedObject = Object.fromEntries(sortedEntries);
console.log(sortedObject);
// { a: 'one', b: 'two', c: 'three' }
```

**Using the Object.keys() Method**

1. Extract the keys of the object using the Object.keys() method.

```javascript
const object = {
  a: 'one',
  b: 'two',
  c: 'three'
};

const keys = Object.keys(object);
console.log(keys);
// ['a', 'b', 'c']
```

2. Sort the keys by their values using the Array.sort() method.

```javascript
const sortedKeys = keys.sort((keyA, keyB) => {
  const valueA = object[keyA];
  const valueB = object[keyB];

  if (valueA < valueB) {
    return -1;
  }
  if (valueA > valueB) {
    return 1;
  }
  return 0;
});
console.log(sortedKeys);
// ['a', 'b', 'c']
```

3. Create a new object from the sorted keys and their corresponding values.

```javascript
const sortedObject = {};
for (const key of sortedKeys) {
  sortedObject[key] = object[key];
}
console.log(sortedObject);
// { a: 'one', b: 'two', c: 'three' }
```
