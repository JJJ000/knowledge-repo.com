---
title: What is the best way to arrange strings in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Strings can be sorted using the built-in Array.prototype.sort() method.
---

**Contents**

[TOC]

### 1. Using Array.prototype.sort()

Array.prototype.sort() is a mutator method that sorts the elements of an array in place and returns the array. It can be used to sort strings alphabetically.

Syntax:

```javascript
arr.sort([compareFunction])
```

Example:

```javascript
let fruits = ["Banana", "Apple", "Orange"];

fruits.sort(); 
// ["Apple", "Banana", "Orange"]
```

### 2. Using the sort() Method with a Custom Comparison Function

The sort() method can also take a callback function as an argument to define the sorting criteria. This callback function takes two arguments and should return a number.

Syntax:

```javascript
arr.sort(compareFunction)
```

Example:

```javascript
let fruits = ["Banana", "Apple", "Orange"];

fruits.sort(function(a, b){
    if(a < b) return -1;
    if(a > b) return 1;
    return 0;
}); 
// ["Apple", "Banana", "Orange"]
```

### 3. Using the Array.prototype.reverse() Method

The Array.prototype.reverse() method is another mutator method that reverses the order of the elements in an array. It can be used to sort strings in reverse alphabetical order.

Syntax:

```javascript
arr.reverse()
```

Example:

```javascript
let fruits = ["Banana", "Apple", "Orange"];

fruits.reverse(); 
// ["Orange", "Banana", "Apple"]
```

### 4. Using Array.prototype.sort() with the Reverse Option

The sort() method also takes an optional Boolean parameter to specify if the sorting should be done in reverse order.

Syntax:

```javascript
arr.sort(compareFunction, reverse)
```

Example:

```javascript
let fruits = ["Banana", "Apple", "Orange"];

fruits.sort(function(a, b){
    if(a < b) return -1;
    if(a > b) return 1;
    return 0;
}, true); 
// ["Orange", "Banana", "Apple"]
```
