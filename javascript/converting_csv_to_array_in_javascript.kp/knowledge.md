---
title: What is the best way to turn a comma-separated string into an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the split() method to convert a comma-separated string to an array in Javascript.
---

**Contents**

[TOC]

### Using the split() Method
The `split()` method is used to split a string into an array of substrings, and returns the new array. 

Syntax: 
```
string.split(separator, limit)
```

Example: 
```
var str = "Apple,Banana,Kiwi";
var arr = str.split(",");
```

The result of `arr` will be: 
```
["Apple", "Banana", "Kiwi"] 
```

### Using the map() Method
The `map()` method is used to create a new array with the results of calling a provided function on every element in the calling array.

Syntax:
```
var new_array = arr.map(function callback(currentValue[, index[, array]]) {
    // Return element for new_array
}[, thisArg])
```

Example: 
```
var str = "Apple,Banana,Kiwi";
var arr = str.split(",").map(function(item) {
    return item;
});
```

The result of `arr` will be: 
```
["Apple", "Banana", "Kiwi"] 
```

### Using the for Loop
The `for` loop is used to iterate over the elements of an array and add them to a new array.

Syntax:
```
for (initialization; condition; final-expression) {
    // code to be executed
}
```

Example:
```
var str = "Apple,Banana,Kiwi";
var arr = str.split(",");
var newArr = [];

for (var i = 0; i < arr.length; i++) {
    newArr.push(arr[i]);
}
```

The result of `newArr` will be: 
```
["Apple", "Banana", "Kiwi"] 
```

### Using the reduce() Method
The `reduce()` method is used to apply a function to each element in the array to reduce it to a single value.

Syntax:
```
arr.reduce(callback( accumulator, currentValue[, index[, array]] )[, initialValue])
```

Example:
```
var str = "Apple,Banana,Kiwi";
var arr = str.split(",");

var newArr = arr.reduce(function(acc, curr) {
    acc.push(curr);
    return acc;
}, []);
```

The result of `newArr` will be: 
```
["Apple", "Banana", "Kiwi"] 
```
