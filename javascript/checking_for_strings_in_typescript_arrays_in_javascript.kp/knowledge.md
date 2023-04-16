---
title: What is the process for determining if a string exists in an array in typescript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Array.prototype.includes() method.
---

**Contents**

[TOC]

#1 Using the Includes Method 
The includes() method can be used to check if a string is present in an array. This method returns true if the given string is found in the array and false if it is not.

Syntax:
array.includes(string);

Example:
let arr = ["apple", "orange", "banana"];
let str = "orange";
arr.includes(str); // returns true

#2 Using the IndexOf Method
The indexOf() method can also be used to check if a string is present in an array. This method searches for the given string in the array and returns its index if found, and -1 if not found.

Syntax:
array.indexOf(string);

Example:
let arr = ["apple", "orange", "banana"];
let str = "orange";
arr.indexOf(str); // returns 1

#3 Using the Find Method
The find() method can be used to check if a string is present in an array. This method searches for the given string in the array and returns its value if found, and undefined if not found.

Syntax:
array.find(string);

Example:
let arr = ["apple", "orange", "banana"];
let str = "orange";
arr.find(str); // returns "orange"

#4 Using the Filter Method
The filter() method can also be used to check if a string is present in an array. This method searches for the given string in the array and returns a new array with all the elements that match the given string.

Syntax:
array.filter(string);

Example:
let arr = ["apple", "orange", "banana"];
let str = "orange";
arr.filter(str); // returns ["orange"]
