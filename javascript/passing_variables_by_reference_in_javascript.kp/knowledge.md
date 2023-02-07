---
title: Reference variables in JavaScript using pass-by-reference
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Variables can be passed by reference in JavaScript by using the `&` operator.
---

**Contents**

[TOC]

## Using Function Parameters

JavaScript allows you to pass variables by reference to functions using function parameters. When a variable is passed as an argument to a function, the function can modify the value of the variable. This is because the function is operating on the same memory address as the original variable.

```javascript
let num = 0;

function increment(numRef) {
  numRef.value += 1;
}

increment(num);
console.log(num); // Output: 1
```

## Using Objects

JavaScript also allows you to pass objects by reference. When an object is passed as an argument to a function, the function can modify the properties of the object. This is because the function is operating on the same memory address as the original object.

```javascript
let obj = {
  value: 0
};

function increment(objRef) {
  objRef.value += 1;
}

increment(obj);
console.log(obj.value); // Output: 1
```

## Using Arrays

JavaScript also allows you to pass arrays by reference. When an array is passed as an argument to a function, the function can modify the elements of the array. This is because the function is operating on the same memory address as the original array.

```javascript
let arr = [0];

function increment(arrRef) {
  arrRef[0] += 1;
}

increment(arr);
console.log(arr[0]); // Output: 1
```

## Using Spread Operator

JavaScript also allows you to pass variables by reference using the spread operator. When a variable is passed as an argument to a function using the spread operator, the function can modify the value of the variable. This is because the function is operating on the same memory address as the original variable.

```javascript
let num = 0;

function increment(...numRef) {
  numRef[0] += 1;
}

increment(num);
console.log(num); // Output: 1
```
