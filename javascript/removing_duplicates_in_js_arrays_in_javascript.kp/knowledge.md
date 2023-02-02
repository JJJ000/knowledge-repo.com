---
title: Retrieve all distinct elements in a JavaScript array (eliminate duplicates)
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the Set object to remove duplicate values from an array.
---

**Contents**

[TOC]

#### Using Set

Set is a new data structure introduced in ES6 which lets you store unique values of any type. We can use the Set object to store the array elements and then get the unique values.

```
let arr = [1, 2, 3, 4, 1, 2, 3, 4];
let uniqueValues = [...new Set(arr)];
console.log(uniqueValues); // [1, 2, 3, 4]
```

#### Using Filter

We can also use the filter function to get the unique values from an array.

```
let arr = [1, 2, 3, 4, 1, 2, 3, 4];
let uniqueValues = arr.filter((value, index, self) => {
  return self.indexOf(value) === index;
});
console.log(uniqueValues); // [1, 2, 3, 4]
```

#### Using Reduce

The reduce() method is used to apply a function to each element in the array to reduce the array to a single value.

```
let arr = [1, 2, 3, 4, 1, 2, 3, 4];
let uniqueValues = arr.reduce((acc, cur) => {
  if (acc.indexOf(cur) < 0) {
    acc.push(cur);
  }
  return acc;
}, []);
console.log(uniqueValues); // [1, 2, 3, 4]
```

#### Using For Loop

We can also use a for loop to iterate over the array and get the unique elements.

```
let arr = [1, 2, 3, 4, 1, 2, 3, 4];
let uniqueValues = [];
for(let i = 0; i < arr.length; i++) {
  if(uniqueValues.indexOf(arr[i]) === -1) {
    uniqueValues.push(arr[i]);
  }
}
console.log(uniqueValues); // [1, 2, 3, 4]
```
