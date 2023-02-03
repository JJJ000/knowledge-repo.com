---
title: What is the best way to eliminate all duplicate objects in an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.filter() method to create a new array with only unique objects based on a certain property.
---

**Contents**

[TOC]

### 1. Using Set
The Set object lets you store unique values of any type, whether primitive values or object references. One way to remove duplicates from an array of objects is to convert the array into a Set, which removes any duplicate objects.

```
let arr = [{name: 'John', age: 20}, {name: 'John', age: 20}, {name: 'Jane', age: 25}]
let uniqueArr = [...new Set(arr)]
```

### 2. Using Filter
Another way to remove duplicates from an array of objects is to use the `filter` method. The `filter` method creates a new array with all elements that pass the test implemented by the provided function. 

```
let arr = [{name: 'John', age: 20}, {name: 'John', age: 20}, {name: 'Jane', age: 25}]
let uniqueArr = arr.filter((item, index) => arr.indexOf(item) === index)
```

### 3. Using Reduce
The `reduce` method can also be used to remove duplicates from an array of objects. The `reduce` method applies a function against an accumulator and each element in the array to reduce it to a single value.

```
let arr = [{name: 'John', age: 20}, {name: 'John', age: 20}, {name: 'Jane', age: 25}]
let uniqueArr = arr.reduce((unique, item) =>
  unique.includes(item) ? unique : [...unique, item], [])
```

### 4. Using For Loop
Finally, a `for` loop can also be used to remove duplicates from an array of objects. The `for` loop iterates over the array and checks if the current element is already present in the new array. If not, it adds it to the new array. 

```
let arr = [{name: 'John', age: 20}, {name: 'John', age: 20}, {name: 'Jane', age: 25}]
let uniqueArr = [];
for (let i = 0; i < arr.length; i++) {
  let current = arr[i];
  if (!uniqueArr.includes(current)) {
    uniqueArr.push(current);
  }
}
```
