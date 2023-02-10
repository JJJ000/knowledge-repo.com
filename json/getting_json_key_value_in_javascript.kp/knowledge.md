---
title: What is the best way to access a JSON key and value using javascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the Object.keys() and Object.values() methods to get the JSON key and value in javascript.
---

**Contents**

[TOC]

1. Using `Object.keys()` 
   - The `Object.keys()` method can be used to get the keys of a JSON object. 
   - Syntax: `Object.keys(object)` 
   - Example: 
   ```
   const jsonObj = {
     "name": "John Doe",
     "age": 25
   };
   
   const keys = Object.keys(jsonObj);
   console.log(keys); // Output: ["name", "age"]
   ```

2. Using `for...in` Loop 
   - The `for...in` loop can be used to loop through the keys of a JSON object. 
   - Syntax: 
   ```
   for (let key in object) {
     // code to be executed
   }
   ```
   - Example: 
   ```
   const jsonObj = {
     "name": "John Doe",
     "age": 25
   };
   
   for (let key in jsonObj) {
     console.log(key + ": " + jsonObj[key]);
   }
   // Output: name: John Doe
   //         age: 25
   ```
