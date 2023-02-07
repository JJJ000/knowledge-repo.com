---
title: What is the best way to arrange an array of objects based on multiple criteria?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Array.prototype.sort() method with a custom compare function to sort an array of objects by multiple fields.
---

**Contents**

[TOC]

### 1. Using `sort`

The `sort` method can be used to sort an array of objects by multiple fields. The `sort` method takes a function as an argument which specifies the order of sorting. 

For example, to sort an array of objects by two fields, `name` and `age`, in ascending order, the following code can be used:

```javascript
const sortedArray = array.sort((a, b) => {
  if (a.name === b.name) {
    return a.age - b.age;
  }
  return a.name.localeCompare(b.name);
});
```

### 2. Using `Array.prototype.reduce`

The `Array.prototype.reduce` method can also be used to sort an array of objects by multiple fields. This method takes a function as an argument which specifies the order of sorting. 

For example, to sort an array of objects by two fields, `name` and `age`, in ascending order, the following code can be used:

```javascript
const sortedArray = array.reduce((acc, obj) => {
  const key = `${obj.name}_${obj.age}`;
  acc[key] = obj;
  return acc;
}, {});
```

### 3. Using Lodash

The Lodash library provides a `orderBy` method which can be used to sort an array of objects by multiple fields. This method takes an array of objects and an array of fields as arguments and sorts the objects based on the specified fields. 

For example, to sort an array of objects by two fields, `name` and `age`, in ascending order, the following code can be used:

```javascript
const sortedArray = _.orderBy(array, ['name', 'age'], ['asc', 'asc']);
```

### 4. Using Underscore

Similar to Lodash, the Underscore library provides an `sortBy` method which can be used to sort an array of objects by multiple fields. This method takes an array of objects and an array of fields as arguments and sorts the objects based on the specified fields. 

For example, to sort an array of objects by two fields, `name` and `age`, in ascending order, the following code can be used:

```javascript
const sortedArray = _.sortBy(array, ['name', 'age']);
```
