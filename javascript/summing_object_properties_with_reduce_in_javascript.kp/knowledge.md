---
title: What is the syntax for using reduce to add the values of a property from an array of objects?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can call reduce on an array of objects to sum their properties by providing a callback function that returns the sum of the current object`s property and the accumulator.
---

**Contents**

[TOC]

### 1. Define the Array

First, define an array of objects with the properties you want to sum. For example, the following array consists of objects with two properties each, `quantity` and `price`:

```javascript
const items = [
  { quantity: 2, price: 10 },
  { quantity: 3, price: 20 },
  { quantity: 4, price: 30 },
];
```

### 2. Define the Reducer Function

Next, define a reducer function that will be used to sum the properties. The reducer function takes two arguments, the accumulator and the current value. The accumulator is used to store the sum of the properties, and the current value is used to access the properties of the current object in the array. In this example, the reducer function will sum the `quantity` and `price` properties of each object in the array:

```javascript
const reducer = (accumulator, currentValue) => {
  return {
    quantity: accumulator.quantity + currentValue.quantity,
    price: accumulator.price + currentValue.price,
  };
};
```

### 3. Call the Reduce Method

Finally, call the `reduce()` method on the array of objects, passing in the reducer function as an argument. This will return an object with the sum of the `quantity` and `price` properties of all the objects in the array:

```javascript
const result = items.reduce(reducer);
console.log(result); // { quantity: 9, price: 60 }
```

### 4. Optional: Initial Value

If you want to set an initial value for the accumulator, you can pass it as the second argument to the `reduce()` method. For example, if you wanted to set the initial value of the accumulator to an object with the `quantity` and `price` properties set to 0, you can do so like this:

```javascript
const initialValue = { quantity: 0, price: 0 };
const result = items.reduce(reducer, initialValue);
console.log(result); // { quantity: 9, price: 60 }
```
