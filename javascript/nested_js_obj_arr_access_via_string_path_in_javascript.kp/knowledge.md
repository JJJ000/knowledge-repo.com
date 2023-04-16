---
title: Retrieving nested JavaScript objects and arrays using a string path
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Objects and arrays can be accessed by using the dot notation or bracket notation to traverse the object`s properties.
---

**Contents**

[TOC]

#### Section 1: Accessing Nested Objects

Nested objects can be accessed using dot notation. For example, if you have an object with a nested object inside of it, you can access the nested object's properties by using dot notation.

```javascript
const obj = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'New York'
  }
}

// Accessing the nested object's properties
const street = obj.address.street // returns '123 Main St'
const city = obj.address.city // returns 'New York'
```

#### Section 2: Accessing Nested Arrays

Nested arrays can be accessed using bracket notation. For example, if you have an array with a nested array inside of it, you can access the nested array's elements by using bracket notation.

```javascript
const arr = [1, 2, [3, 4, 5]];

// Accessing the nested array's elements
const firstElement = arr[0] // returns 1
const secondElement = arr[1] // returns 2
const thirdElement = arr[2][0] // returns 3
const fourthElement = arr[2][1] // returns 4
const fifthElement = arr[2][2] // returns 5
```

#### Section 3: Accessing Nested Objects and Arrays

Nested objects and arrays can be accessed by using a combination of dot and bracket notation. For example, if you have an object with a nested array inside of it, you can access the nested array's elements by using dot and bracket notation.

```javascript
const obj = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'New York',
    numbers: [1, 2, 3]
  }
}

// Accessing the nested array's elements
const firstNumber = obj.address.numbers[0] // returns 1
const secondNumber = obj.address.numbers[1] // returns 2
const thirdNumber = obj.address.numbers[2] // returns 3
```

#### Section 4: Accessing Nested Objects and Arrays by String Path

Nested objects and arrays can also be accessed by using a string path. For example, if you have an object with a nested array inside of it, you can access the nested array's elements by using a string path.

```javascript
const obj = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'New York',
    numbers: [1, 2, 3]
  }
}

// Accessing the nested array's elements
const firstNumber = get(obj, 'address.numbers[0]') // returns 1
const secondNumber = get(obj, 'address.numbers[1]') // returns 2
const thirdNumber = get(obj, 'address.numbers[2]') // returns 3
```

The `get` function is a function that takes in an object and a string path and returns the value of the element at the given path.
