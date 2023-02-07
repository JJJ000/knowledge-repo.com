---
title: Verify if an object exists in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can check if an object exists in JavaScript by using the `typeof` operator.
---

**Contents**

[TOC]

# Using the `typeof` Operator
The `typeof` operator is used to check if an object exists in JavaScript. This operator will return the type of the object, or `undefined` if the object does not exist. 

Example: 
```
let myObject = {};

if (typeof myObject !== 'undefined') {
  // Do something with myObject
}
```

# Using the `in` Operator
The `in` operator is used to check if an object has a property. This operator will return `true` if the object has the specified property, or `false` if the object does not have the specified property. 

Example: 
```
let myObject = {
  name: 'John'
};

if ('name' in myObject) {
  // Do something with myObject.name
}
```

# Using the `hasOwnProperty()` Method
The `hasOwnProperty()` method is used to check if an object has a property. This method will return `true` if the object has the specified property, or `false` if the object does not have the specified property. 

Example: 
```
let myObject = {
  name: 'John'
};

if (myObject.hasOwnProperty('name')) {
  // Do something with myObject.name
}
```
