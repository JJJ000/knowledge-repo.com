---
title: Searching for values within a JavaScript object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, it is possible to search for values in a JSON object using the JavaScript `JSON.search()` method.
---

**Contents**

[TOC]

1. Using `Object.values()` 

The `Object.values()` method returns an array of a given object's own enumerable property values, in the same order as that provided by a `for...in` loop.

Syntax: 
```
Object.values(obj)
```

Example:
```
let object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.values(object1));
// expected output: Array ["somestring", 42, false]
```

2. Using `for..in` Loop

The `for..in` loop is used to iterate over the enumerable properties of an object, in an arbitrary order.

Syntax: 
```
for (variable in object) {
  // code block to be executed
}
```

Example:
```
let object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

for (const value in object1) {
  console.log(object1[value]);
}
// expected output: somestring 42 false
```
