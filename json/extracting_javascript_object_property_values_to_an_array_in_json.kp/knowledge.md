---
title: What is the best way to convert the property values of a JavaScript object into an array?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can use the Object.values() method to extract the property values of a JavaScript object into an array in JSON.
---

**Contents**

[TOC]

1. Using `Object.values()`
  
   The `Object.values()` method can be used to return an array of a given object's own enumerable property values, in the same order as that provided by a `for...in` loop.
  
  ```javascript
  let myObj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
  };
  
  let values = Object.values(myObj);
  console.log(values); // ['value1', 'value2', 'value3']
  ```

2. Using `Object.entries()`
  
   The `Object.entries()` method can be used to return an array of a given object's own enumerable property [key, value] pairs.
  
  ```javascript
  let myObj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
  };
  
  let entries = Object.entries(myObj);
  console.log(entries); // [['prop1', 'value1'], ['prop2', 'value2'], ['prop3', 'value3']]
  ```

3. Using `for...in` Loop
  
   The `for...in` loop can be used to iterate over the enumerable properties of an object, and extract their values into an array.
  
  ```javascript
  let myObj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
  };
  
  let values = [];
  for (let key in myObj) {
    values.push(myObj[key]);
  }
  console.log(values); // ['value1', 'value2', 'value3']
  ```

4. Using `Object.keys()`
  
   The `Object.keys()` method can be used to return an array of a given object's own enumerable property names. We can then use this array of keys to access the object's values and push them into an array.
  
  ```javascript
  let myObj = {
    prop1: 'value1',
    prop2: 'value2',
    prop3: 'value3'
  };
  
  let keys = Object.keys(myObj);
  let values = [];
  keys.forEach(key => {
    values.push(myObj[key]);
  });
  console.log(values); // ['value1', 'value2', 'value3']
  ```
