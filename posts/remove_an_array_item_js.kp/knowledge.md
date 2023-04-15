---
title: What is the syntax for removing a specific item from an array in JavaScript?
authors:
- cool_wizard
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: There are a few methods to use, including `splice()`, `filter()`, `indexOf()`, or `findIndex()`
---

**Contents**

[TOC]


There are several ways to remove a specific item from an array in JavaScript:

### Using the splice() method

```JS
let numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 1);  // removes the element at index 2 (i.e., 3)
console.log(numbers);  // [1, 2, 4, 5]
```

### Using the filter() method

```JS
let numbers = [1, 2, 3, 4, 5];
numbers = numbers.filter(x => x !== 3);  // removes the element with value 3
console.log(numbers);  // [1, 2, 4, 5]
```

### Using the indexOf() method

```JS
let numbers = [1, 2, 3, 4, 5];
let index = numbers.indexOf(3);
if (index !== -1) {
    numbers.splice(index, 1);  // removes the element with value 3
}
console.log(numbers);  // [1, 2, 4, 5]
```

### Using the findIndex() method

```JS
let numbers = [1, 2, 3, 4, 5];
let index = numbers.findIndex(x => x === 3);
if (index !== -1) {
    numbers.splice(index, 1);  // removes the element with value 3
}
console.log(numbers);  // [1, 2, 4, 5]
```

Which method you choose to use depends on your specific use case. The `splice()` method is good for removing an element at a specific index, while the `filter()`, `indexOf()`, and `findIndex()` methods are good for removing an element with a specific value.
