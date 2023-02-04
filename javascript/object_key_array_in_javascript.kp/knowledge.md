---
title: Retrieve an array of the object's keys
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Object.keys(object) returns an array of the object`s keys.
---

**Contents**

[TOC]

1. Using `Object.keys()`
 
   `Object.keys()` is a built-in method in JavaScript which returns an array of the given object's own enumerable properties. It takes the object as an argument and returns its keys in an array. 
   
   **Syntax:**
   ```
   Object.keys(object)
   ```

2. Using `for...in` loop
 
   `for...in` loop is used to iterate over the enumerable properties of an object, thus returning the object's keys in an array.
   
   **Syntax:**
   ```
   for (let key in object) {
     // do something with the key
   }
   ```

3. Using `Object.getOwnPropertyNames()`
 
   `Object.getOwnPropertyNames()` is a built-in method in JavaScript which returns an array of all properties (enumerable or non-enumerable) found directly upon a given object. 
   
   **Syntax:**
   ```
   Object.getOwnPropertyNames(object)
   ```

4. Using `Object.entries()`
 
   `Object.entries()` is a built-in method in JavaScript which returns an array of a given object's own enumerable string-keyed property [key, value] pairs. It takes the object as an argument and returns its keys in an array. 
   
   **Syntax:**
   ```
   Object.entries(object)
   ```
