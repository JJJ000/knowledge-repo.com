---
title: Create an array containing the values of a specific property from an array of objects
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the Array.map() method to extract the value of a property as an array from an array of objects.
---

**Contents**

[TOC]

**Section 1: Introduction**

Extracting values from an array of objects can be done using various methods. This article will discuss two methods for extracting values from an array of objects in JavaScript.

**Section 2: Using the `map()` Method**

The `map()` method can be used to extract values from an array of objects. This method takes a callback function as an argument and returns a new array containing the results of the callback function. The callback function takes three arguments: the current value, the index of the current value, and the array being mapped. The value of the property can be accessed by using the dot notation on the object.

For example, let's say we have an array of objects with a property called `name`:

```javascript
const arr = [
  { name: 'John' },
  { name: 'Jane' },
  { name: 'Jack' }
];
```

We can use the `map()` method to extract the values of the `name` property:

```javascript
const names = arr.map(obj => obj.name);

// names = ['John', 'Jane', 'Jack']
```

**Section 3: Using the `reduce()` Method**

The `reduce()` method can also be used to extract values from an array of objects. This method takes a callback function as an argument and returns a single value (or object) containing the results of the callback function. The callback function takes four arguments: the accumulator, the current value, the index of the current value, and the array being reduced. The value of the property can be accessed by using the dot notation on the object.

For example, let's say we have an array of objects with a property called `name`:

```javascript
const arr = [
  { name: 'John' },
  { name: 'Jane' },
  { name: 'Jack' }
];
```

We can use the `reduce()` method to extract the values of the `name` property:

```javascript
const names = arr.reduce((acc, obj) => {
  acc.push(obj.name);
  return acc;
}, []);

// names = ['John', 'Jane', 'Jack']
```

**Section 4: Conclusion**

In conclusion, extracting values from an array of objects can be done using either the `map()` or `reduce()` methods. Both methods take a callback function as an argument, and the value of the property can be accessed by using the dot notation on the object.
