---
title: Arrange the objects in the array in order of their string property values
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the Array.prototype.sort() method with a custom comparison function to sort the array of objects by string property value.
---

**Contents**

[TOC]

### Solution 1:

Using the `Array.prototype.sort()` method:

```javascript
let arr = [
    {name: "John", age: 24},
    {name: "Bob", age: 22},
    {name: "Alice", age: 21},
    {name: "Eve", age: 25}
];

arr.sort((a, b) => (a.name > b.name) ? 1 : -1);

console.log(arr);
// [
//   { name: 'Alice', age: 21 },
//   { name: 'Bob', age: 22 },
//   { name: 'Eve', age: 25 },
//   { name: 'John', age: 24 }
// ]
```

### Solution 2:

Using the `Array.prototype.sort()` method with a custom comparison function:

```javascript
let arr = [
    {name: "John", age: 24},
    {name: "Bob", age: 22},
    {name: "Alice", age: 21},
    {name: "Eve", age: 25}
];

arr.sort((a, b) => {
    let nameA = a.name.toUpperCase();
    let nameB = b.name.toUpperCase();
    if (nameA < nameB) {
        return -1;
    }
    if (nameA > nameB) {
        return 1;
    }
    return 0;
});

console.log(arr);
// [
//   { name: 'Alice', age: 21 },
//   { name: 'Bob', age: 22 },
//   { name: 'Eve', age: 25 },
//   { name: 'John', age: 24 }
// ]
```

### Solution 3:

Using the `Array.prototype.map()` and `Array.prototype.sort()` methods:

```javascript
let arr = [
    {name: "John", age: 24},
    {name: "Bob", age: 22},
    {name: "Alice", age: 21},
    {name: "Eve", age: 25}
];

let sortedArr = arr.map(a => a.name).sort();

let result = sortedArr.map(name => {
    return arr.find(a => a.name === name);
});

console.log(result);
// [
//   { name: 'Alice', age: 21 },
//   { name: 'Bob', age: 22 },
//   { name: 'Eve', age: 25 },
//   { name: 'John', age: 24 }
// ]
```

### Solution 4:

Using the `Array.prototype.reduce()` and `Array.prototype.sort()` methods:

```javascript
let arr = [
    {name: "John", age: 24},
    {name: "Bob", age: 22},
    {name: "Alice", age: 21},
    {name: "Eve", age: 25}
];

let result = arr.sort((a, b) => (a.name > b.name) ? 1 : -1).reduce((acc, cur) => {
    acc.push(cur);
    return acc;
}, []);

console.log(result);
// [
//   { name: 'Alice', age: 21 },
//   { name: 'Bob', age: 22 },
//   { name: 'Eve', age: 25 },
//   { name: 'John', age: 24 }
// ]
```
