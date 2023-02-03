---
title: Delete empty elements from an array in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the Array.filter() method to remove empty elements from an array in Javascript.
---

**Contents**

[TOC]

**1. Using for Loop**

```javascript
let array = [1, 2, 3, 0, "", 4, 5, null, undefined];

for (let i = 0; i < array.length; i++) {
    if (array[i] === "" || array[i] === null || array[i] === undefined) {
        array.splice(i, 1);
        i--;
    }
}

console.log(array); // [1, 2, 3, 4, 5]
```

**2. Using Filter Method**

```javascript
let array = [1, 2, 3, 0, "", 4, 5, null, undefined];

let filteredArray = array.filter(function(element) {
    return element !== "" && element !== null && element !== undefined;
});

console.log(filteredArray); // [1, 2, 3, 4, 5]
```

**3. Using ES6 Syntax**

```javascript
let array = [1, 2, 3, 0, "", 4, 5, null, undefined];

let filteredArray = array.filter(element => element !== "" && element !== null && element !== undefined);

console.log(filteredArray); // [1, 2, 3, 4, 5]
```

**4. Using Reduce Method**

```javascript
let array = [1, 2, 3, 0, "", 4, 5, null, undefined];

let filteredArray = array.reduce(function(accumulator, currentValue) {
    if (currentValue !== "" && currentValue !== null && currentValue !== undefined) {
        accumulator.push(currentValue);
    }
    return accumulator;
}, []);

console.log(filteredArray); // [1, 2, 3, 4, 5]
```
