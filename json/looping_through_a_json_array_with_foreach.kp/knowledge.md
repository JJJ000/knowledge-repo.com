---
title: For every element in a JSON array, the syntax is
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The syntax for looping through a JSON array is `foreach (var item in array) { //code here }`.
---

**Contents**

[TOC]

**Section 1: Basics of JSON**

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write, and easy for machines to parse and generate. JSON is based on a subset of the JavaScript Programming Language, Standard ECMA-262 3rd Edition - December 1999.

**Section 2: JSON Array Syntax**

A JSON array is an ordered list of values. An array begins with a left bracket [ and ends with a right bracket ]. Values are separated by a comma ,.

The syntax for a JSON array is as follows:

```json
[
    value1,
    value2,
    ...
    valueN
]
```

**Section 3: Foreach for JSON Array**

A foreach loop can be used to iterate through a JSON array. The syntax for a foreach loop is as follows:

```javascript
array.forEach(function(value, index, array) {
    // Code to be executed
});
```

**Section 4: Example of Foreach for JSON Array**

Here is an example of a foreach loop that iterates through a JSON array:

```javascript
var jsonArray = [1,2,3,4,5];

jsonArray.forEach(function(value, index, array) {
    console.log(value);
});

// Output:
// 1
// 2
// 3
// 4
// 5
```
