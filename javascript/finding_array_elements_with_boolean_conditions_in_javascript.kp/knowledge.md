---
title: What is the syntax to locate the first element in a JavaScript array that meets a specified boolean condition?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Array.prototype.find() method to find the first element of an array matching a boolean condition.
---

**Contents**

[TOC]

### Using for Loop

We can use a for loop to loop through the array and find the first element that matches the boolean condition.

```javascript
var array = [1, 2, 3, 4, 5];
var condition = 3;

for (var i = 0; i < array.length; i++) {
  if (array[i] == condition) {
    console.log(array[i]);
    break;
  }
}

// Output: 3
```

### Using find() Method

We can also use the find() method to find the first element of the array that matches the boolean condition.

```javascript
var array = [1, 2, 3, 4, 5];
var condition = 3;

var result = array.find(function(element) {
  return element == condition;
});

console.log(result);

// Output: 3
```
