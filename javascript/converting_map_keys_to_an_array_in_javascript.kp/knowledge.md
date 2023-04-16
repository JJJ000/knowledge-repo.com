---
title: What is the process for turning map keys into an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Object.keys() method to convert Map keys to an array in Javascript.
---

**Contents**

[TOC]

### Section 1 - Creating a Map

A Map is a collection of key-value pairs in Javascript. It is similar to an object, but the main difference is that the keys of a Map can be any data type, while the keys of an object must be strings or symbols.

To create a Map in Javascript, you can use the `Map()` constructor.

```javascript
let myMap = new Map();
```

### Section 2 - Adding Key-Value Pairs to a Map

You can add key-value pairs to a Map using the `set()` method.

```javascript
myMap.set('name', 'John');
myMap.set('age', 20);
myMap.set('location', 'New York');
```

### Section 3 - Converting Map Keys to an Array

To convert the keys of a Map to an array, you can use the `keys()` method. This method returns an iterator object containing the keys of the Map.

```javascript
let myMapKeys = Array.from(myMap.keys());
```

### Section 4 - Accessing the Array

The `myMapKeys` variable now contains an array of the keys of the Map. You can access the array elements using array notation.

```javascript
console.log(myMapKeys[0]); // Outputs "name"
console.log(myMapKeys[1]); // Outputs "age"
console.log(myMapKeys[2]); // Outputs "location"
```
