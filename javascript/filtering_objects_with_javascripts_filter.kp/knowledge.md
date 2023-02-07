---
title: Using javascript's filter() method on objects
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The filter() method creates a new array with all elements that pass the test implemented by the provided function.
---

**Contents**

[TOC]

# Overview
The `filter()` method is used to create a new array with all elements that pass the test implemented by the provided function. This method is available for both objects and arrays in JavaScript. 

# Syntax
The syntax for `filter()` when used with objects is as follows: 

```javascript
const newArray = Object.keys(object).filter(function(key) {
  return object[key];
});
```

# Example
Suppose we have an object like this: 

```javascript
const object = {
  name: "John",
  age: 30,
  job: "programmer"
};
```

We can use `filter()` to create a new array that only contains the keys of the object for which the value is truthy: 

```javascript
const newArray = Object.keys(object).filter(function(key) {
  return object[key];
});

console.log(newArray); // ["name", "age", "job"]
```

# Conclusion
The `filter()` method is a useful tool for creating a new array from an object with only elements that pass the test implemented by the provided function.
