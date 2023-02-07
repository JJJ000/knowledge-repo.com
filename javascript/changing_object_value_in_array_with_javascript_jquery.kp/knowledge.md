---
title: What is the syntax for altering an object's value within an array using JavaScript or jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Using the array index, you can access the object and set a new value for the desired property.
---

**Contents**

[TOC]

### Section 1: Using JavaScript

1. First, access the array containing the object.
2. Use the `for` loop to iterate through the array and look for the desired object.
3. Once the desired object is found, use the dot notation to access the property of the object that needs to be changed.
4. Assign the new value to the property.

### Section 2: Using jQuery

1. Access the array containing the object.
2. Use the `$.each()` method to iterate through the array and look for the desired object.
3. Once the desired object is found, use the `$.prop()` method to access the property of the object that needs to be changed.
4. Assign the new value to the property.
