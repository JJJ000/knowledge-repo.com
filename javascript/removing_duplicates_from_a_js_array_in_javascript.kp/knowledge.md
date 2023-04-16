---
title: Eliminate repeated elements from a JavaScript array
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Array.prototype.filter() method to filter out duplicate values from a JavaScript array.
---

**Contents**

[TOC]

# Solution 1 - Using Set 

Using the Set object, we can remove duplicate values from an array by first converting the array into a Set object and then converting it back into an array.

```javascript
let arr = [1,2,3,4,4,4,5,6,7,7];

let uniqueArr = [...new Set(arr)];

console.log(uniqueArr); // [1,2,3,4,5,6,7]
```

# Solution 2 - Using Filter

We can also use the `Array.prototype.filter()` method to filter out duplicate values from an array.

```javascript
let arr = [1,2,3,4,4,4,5,6,7,7];

let uniqueArr = arr.filter( (value, index, self) => {
  return self.indexOf(value) === index;
});

console.log(uniqueArr); // [1,2,3,4,5,6,7]
```

# Solution 3 - Using Reduce

We can also use the `Array.prototype.reduce()` method to filter out duplicate values from an array.

```javascript
let arr = [1,2,3,4,4,4,5,6,7,7];

let uniqueArr = arr.reduce( (acc, curr) => {
  if (acc.indexOf(curr) < 0) {
    acc.push(curr);
  }
  return acc;
}, []);

console.log(uniqueArr); // [1,2,3,4,5,6,7]
```

# Solution 4 - Using For Loop

We can also use a simple `for` loop to filter out duplicate values from an array.

```javascript
let arr = [1,2,3,4,4,4,5,6,7,7];

let uniqueArr = [];

for (let i = 0; i < arr.length; i++) {
  if (uniqueArr.indexOf(arr[i]) < 0) {
    uniqueArr.push(arr[i]);
  }
}

console.log(uniqueArr); // [1,2,3,4,5,6,7]
```
