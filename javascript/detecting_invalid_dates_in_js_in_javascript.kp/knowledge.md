---
title: Identifying an incorrect date in a JavaScript date object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can detect an invalid date by checking if the Date instance is equal to the Date instance of `Invalid Date`.
---

**Contents**

[TOC]

### Using the Date.prototype.toString() Method

The Date.prototype.toString() method can be used to detect an invalid Date instance in JavaScript. If the Date instance is invalid, the method will return a string containing the value "Invalid Date". 

### Using the Date.prototype.getTime() Method 

The Date.prototype.getTime() method can also be used to detect an invalid Date instance in JavaScript. If the Date instance is invalid, the method will return the value NaN (Not a Number). 

### Using the Date.prototype.valueOf() Method 

The Date.prototype.valueOf() method can also be used to detect an invalid Date instance in JavaScript. If the Date instance is invalid, the method will return the value NaN (Not a Number). 

### Using the isNaN() Function 

The isNaN() function can also be used to detect an invalid Date instance in JavaScript. If the Date instance is invalid, the isNaN() function will return true.
