---
title: What is the best way to iterate over a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can loop through a JavaScript object using a for-in loop.
---

**Contents**

[TOC]

**For-in loop**

A `for-in` loop is the most common way to loop through an object in JavaScript. This loop iterates over the object's properties and allows you to access the values associated with each property. 

Syntax: 
```
for (var key in object) {
  // code to be executed
}
```
Example: 
```
var obj = {a:1, b:2, c:3};

for (var prop in obj) {
  console.log("obj." + prop + " = " + obj[prop]);
}

// Output:
// obj.a = 1
// obj.b = 2
// obj.c = 3
```

**Object.keys()**

The `Object.keys()` method returns an array of a given object's own enumerable property names. This can be used to loop through an object's properties. 

Syntax:
```
Object.keys(objectName)
```
Example:
```
var obj = {a:1, b:2, c:3};
var keys = Object.keys(obj);

for (var i = 0; i < keys.length; i++) {
  console.log(keys[i] + ' = ' + obj[keys[i]]);
}

// Output:
// a = 1
// b = 2
// c = 3
```

**Object.entries()**

The `Object.entries()` method returns an array of a given object's own enumerable property [key, value] pairs. This can be used to loop through an object's properties. 

Syntax:
```
Object.entries(objectName)
```
Example:
```
var obj = {a:1, b:2, c:3};
var entries = Object.entries(obj);

for (var i = 0; i < entries.length; i++) {
  console.log(entries[i][0] + ' = ' + entries[i][1]);
}

// Output:
// a = 1
// b = 2
// c = 3
```

**forEach()**

The `forEach()` method executes a provided function once for each array element. This can be used to loop through an object's properties. 

Syntax:
```
Object.forEach(function(item, index, object) {
  // code to be executed
});
```
Example:
```
var obj = {a:1, b:2, c:3};

Object.keys(obj).forEach(function(key) {
  console.log(key + ' = ' + obj[key]);
});

// Output:
// a = 1
// b = 2
// c = 3
```
