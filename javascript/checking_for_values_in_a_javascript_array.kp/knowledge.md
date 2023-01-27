---
title: What is the procedure to determine if an array contains a specific value in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the Array.prototype.includes() method to check if an array includes a value in JavaScript.
---

**Contents**

[TOC]

### Using the `includes()` Method

The `includes()` method can be used to check if an array includes a certain value. This method returns a boolean value (`true` if the value is found, and `false` if the value is not found).

Syntax:
```
array.includes(valueToFind, startIndex)
```

Example:
```
let array = [1, 2, 3, 4, 5];

array.includes(3);
// returns true

array.includes(6);
// returns false
```

### Using the `indexOf()` Method

The `indexOf()` method can also be used to check if an array includes a certain value. This method returns the index of the element in the array if it is found, or `-1` if it is not found.

Syntax:
```
array.indexOf(valueToFind, startIndex)
```

Example:
```
let array = [1, 2, 3, 4, 5];

array.indexOf(3);
// returns 2

array.indexOf(6);
// returns -1
```

### Using the `for` Loop

The `for` loop can be used to iterate over an array and check if it includes a certain value.

Syntax:
```
for (let i = 0; i < array.length; i++) {
  if (array[i] === valueToFind) {
    // value is found
  }
}
```

Example:
```
let array = [1, 2, 3, 4, 5];
let valueToFind = 3;
let found = false;

for (let i = 0; i < array.length; i++) {
  if (array[i] === valueToFind) {
    found = true;
    break;
  }
}

console.log(found);
// returns true
```
