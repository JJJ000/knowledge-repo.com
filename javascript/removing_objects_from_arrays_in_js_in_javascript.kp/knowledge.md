---
title: Delete an element from an array using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.splice() method to remove an element from an array in JavaScript.
---

**Contents**

[TOC]

## Using splice()
The `splice()` method is used to remove elements from an array. 

Syntax:
```javascript
array.splice(index, howmany, item1, ....., itemX)
```
Parameters:
- index: An integer that specifies at what position to add/remove items, Use negative values to specify the position from the end of the array
- howmany: The number of items to be removed. If set to 0, no items will be removed
- item1, ..., itemX: The new item(s) to be added to the array

Example:
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 1); 
// Removes the second element (Apple) from fruits
```

## Using filter()
The `filter()` method creates a new array with all elements that pass the test implemented by the provided function.

Syntax:
```javascript
array.filter(function(currentValue, index, arr), thisValue)
```
Parameters:
- function(currentValue, index, arr): A function to be run for each element in the array. 
- thisValue: Optional. A value to be passed to the function to be used as its "this" value.

Example:
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var removed = fruits.filter(function(fruit) { 
  return fruit !== "Apple";
});
// Removes the element "Apple" from the array
```

## Using pop()
The `pop()` method removes the last element from an array and returns that element.

Syntax:
```javascript
array.pop()
```

Example:
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var removed = fruits.pop(); 
// Removes the last element (Mango) from the array
```

## Using shift()
The `shift()` method removes the first element from an array and returns that element.

Syntax:
```javascript
array.shift()
```

Example:
```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var removed = fruits.shift(); 
// Removes the first element (Banana) from the array
```
