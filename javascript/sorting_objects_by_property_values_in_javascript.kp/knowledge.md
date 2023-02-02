---
title: Arranging an array of objects according to their property values
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Array.sort() can be used to sort an array of objects by property values.
---

**Contents**

[TOC]

# Section 1: Sorting an Array of Numbers

When sorting an array of numbers, the simplest way to do this is to use the built-in `Array.sort()` method. This method takes a comparison function as an argument, which allows you to specify how the array should be sorted. For example, to sort an array of numbers in ascending order, you could use the following code:

```javascript
let numbers = [4, 2, 5, 1, 3];
numbers.sort(function(a, b) {
  return a - b;
});

// numbers is now [1, 2, 3, 4, 5]
```

# Section 2: Sorting an Array of Strings

Sorting an array of strings is similar to sorting an array of numbers. The `Array.sort()` method can be used, but a different comparison function must be provided. To sort an array of strings in alphabetical order, the following code can be used:

```javascript
let strings = ["b", "d", "a", "c"];
strings.sort(function(a, b) {
  if (a < b) {
    return -1;
  }
  if (a > b) {
    return 1;
  }
  return 0;
});

// strings is now ["a", "b", "c", "d"]
```

# Section 3: Sorting an Array of Objects

Sorting an array of objects requires a slightly more complex comparison function. This is because the comparison function must specify which property of the objects should be used for sorting. For example, to sort an array of objects by their `name` property in alphabetical order, the following code can be used:

```javascript
let people = [
  { name: "Bob", age: 30 },
  { name: "Alice", age: 20 },
  { name: "John", age: 25 }
];
people.sort(function(a, b) {
  if (a.name < b.name) {
    return -1;
  }
  if (a.name > b.name) {
    return 1;
  }
  return 0;
});

// people is now [{ name: "Alice", age: 20 },
//                 { name: "Bob", age: 30 },
//                 { name: "John", age: 25 }]
```

# Section 4: Sorting an Array of Objects by Multiple Properties

It is also possible to sort an array of objects by multiple properties. This requires a more complex comparison function that takes multiple properties into account. For example, to sort an array of objects by their `name` property in alphabetical order, and then by their `age` property in descending order, the following code can be used:

```javascript
let people = [
  { name: "Bob", age: 30 },
  { name: "Alice", age: 20 },
  { name: "John", age: 25 }
];
people.sort(function(a, b) {
  if (a.name < b.name) {
    return -1;
  }
  if (a.name > b.name) {
    return 1;
  }
  if (a.age > b.age) {
    return -1;
  }
  if (a.age < b.age) {
    return 1;
  }
  return 0;
});

// people is now [{ name: "Alice", age: 20 },
//                 { name: "John", age: 25 },
//                 { name: "Bob", age: 30 }]
```
