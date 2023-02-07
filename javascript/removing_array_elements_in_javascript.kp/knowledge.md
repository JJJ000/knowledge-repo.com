---
title: Take out all elements that are present in another array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Array.filter() method to create a new array containing only the elements that are not present in the other array.
---

**Contents**

[TOC]

**1. Using `filter()`**

This method is used to create a new array with all elements that pass the test implemented by the provided function.

```javascript
let array1 = [1, 2, 3, 4, 5];
let array2 = [4, 5, 6, 7, 8];

let result = array1.filter(el => !array2.includes(el));

console.log(result); // [1, 2, 3]
```

**2. Using `reduce()`**

This method is used to apply a function to each element in the array to reduce it to a single value.

```javascript
let array1 = [1, 2, 3, 4, 5];
let array2 = [4, 5, 6, 7, 8];

let result = array1.reduce((acc, el) => {
    if (!array2.includes(el)) acc.push(el);
    return acc;
}, []);

console.log(result); // [1, 2, 3]
```

**3. Using `forEach()`**

This method is used to execute a provided function once for each array element.

```javascript
let array1 = [1, 2, 3, 4, 5];
let array2 = [4, 5, 6, 7, 8];
let result = [];

array1.forEach(el => {
    if (!array2.includes(el)) result.push(el);
});

console.log(result); // [1, 2, 3]
```

**4. Using `for...of`**

This loop is used to iterate over iterable objects such as arrays, strings, and maps.

```javascript
let array1 = [1, 2, 3, 4, 5];
let array2 = [4, 5, 6, 7, 8];
let result = [];

for (let el of array1) {
    if (!array2.includes(el)) result.push(el);
}

console.log(result); // [1, 2, 3]
```
