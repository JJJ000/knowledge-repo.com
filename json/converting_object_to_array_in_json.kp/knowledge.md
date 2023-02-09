---
title: Transforming a JavaScript object with numerical keys into an array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: The JavaScript object with numeric keys can be converted into an array in JSON by using the JSON.stringify() method.
---

**Contents**

[TOC]

# Section 1: Understanding the JavaScript Object

A JavaScript object is a data type that is composed of a collection of key-value pairs. The keys are strings and the values can be any type of data, including other objects. In the case of an object with numeric keys, the keys are strings that represent the numbers.

# Section 2: Converting the Object to an Array

The simplest way to convert an object with numeric keys into an array is to use the `Object.values()` method. This method returns an array containing all the values of the object, in the same order as the keys.

# Section 3: Converting the Array to JSON

Once the object has been converted to an array, it can be converted to JSON using the `JSON.stringify()` method. This method takes the array as an argument and returns a string containing the JSON representation of the array.

# Section 4: Example

Here is an example of how to convert an object with numeric keys into an array and then to JSON:

```
//Create an object with numeric keys
let myObject = {
    '1': 'one',
    '2': 'two',
    '3': 'three'
};

//Convert the object to an array
let myArray = Object.values(myObject);

//Convert the array to JSON
let myJSON = JSON.stringify(myArray);

//Output the JSON
console.log(myJSON);

//Output: ["one", "two", "three"]
```
