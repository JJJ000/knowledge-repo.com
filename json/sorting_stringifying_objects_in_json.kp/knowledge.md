---
title: Arrange object attributes and convert to JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON.stringify is used to convert a JavaScript object into a JSON string, and it can be used to sort the object properties alphabetically.
---

**Contents**

[TOC]

**Sorting Object Properties**

Objects in JavaScript can be sorted in several different ways. The most common way is to use the `Object.keys()` method to get an array of keys, then sort the array, and finally create a new object using the sorted array.

**JSON.stringify()**

The `JSON.stringify()` method converts a JavaScript object or value to a JSON string. This method can take two arguments, the object to be converted, and an optional replacer function that can be used to filter or modify the data before it is stringified.

**Sorting and Stringifying Objects**

When sorting and stringifying objects, the `Object.keys()` method can be used to get an array of the object's keys, which can then be sorted. The sorted array can then be used to create a new object, which can then be stringified using the `JSON.stringify()` method.

**Example**

Below is an example of sorting and stringifying an object:

```
const obj = {
    a: 1,
    b: 2,
    c: 3
};

const sortedKeys = Object.keys(obj).sort();
const sortedObj = {};

sortedKeys.forEach(key => {
    sortedObj[key] = obj[key];
});

const stringifiedObj = JSON.stringify(sortedObj);

console.log(stringifiedObj); // '{"a":1,"b":2,"c":3}'
```
