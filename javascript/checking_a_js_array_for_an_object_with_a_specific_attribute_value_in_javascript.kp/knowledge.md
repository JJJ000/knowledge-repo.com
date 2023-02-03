---
title: What is the best way to check if a JavaScript array includes an object with a specific attribute that has a particular value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Array.prototype.find() method to search the array for an object that has an attribute that equals the given value.
---

**Contents**

[TOC]

**Section 1: Iterate Through Array**

To determine if a Javascript array contains an object with an attribute that equals a given value, you can use a `for` loop to iterate through the array. 

**Section 2: Compare Attribute Value**

Within the loop, you can use an `if` statement to compare the attribute value of each object in the array to the given value. 

**Section 3: Return True or False**

If the attribute value of an object in the array matches the given value, you can return `true`. Otherwise, you can return `false`. 

**Section 4: Example Code**

Below is an example of code that can be used to determine if a Javascript array contains an object with an attribute that equals a given value:

```
function containsObject(arr, value) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i].attribute === value) {
      return true;
    }
  }
  return false;
}
```
