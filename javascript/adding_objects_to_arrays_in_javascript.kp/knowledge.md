---
title: What is the process for adding an item to an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To add an object to an array in Javascript, use the Array.push() method.
---

**Contents**

[TOC]

## 1. Declare the Array

The first step to adding an object to an array is to declare the array. This can be done using the `var` keyword:

```javascript
var myArray = [];
```

## 2. Create the Object

The next step is to create the object that you would like to add to the array. This can be done by defining the object's properties and values:

```javascript
var myObject = {
  name: 'John',
  age: 25
};
```

## 3. Push the Object to the Array

Now that we have declared the array and created the object, we can add the object to the array using the `push()` method:

```javascript
myArray.push(myObject);
```

## 4. Verify the Object is Added

Finally, we can verify that the object is added to the array by logging the array to the console:

```javascript
console.log(myArray);
```
