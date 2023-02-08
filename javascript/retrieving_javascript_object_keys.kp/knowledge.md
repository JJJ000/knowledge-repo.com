---
title: Retrieving a list of keys from a JavaScript object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the Object.keys() method to get a list of the keys of a JavaScript object.
---

**Contents**

[TOC]

##### Using Object.keys()
Object.keys() is a built-in JavaScript function that returns an array of the given object's property names.

Syntax:
```
Object.keys(object)
```

Example:
```
let obj = {
    name: "John",
    age: 30,
    city: "New York"
};

let keys = Object.keys(obj);
// Output: ["name", "age", "city"]
```

##### Using for...in Loop
The for...in loop is another way to iterate over an object's properties. It loops over the object's enumerable properties and returns an array of the object's keys.

Syntax:
```
for (let key in object) {
    // do something with key
}
```

Example:
```
let obj = {
    name: "John",
    age: 30,
    city: "New York"
};

let keys = [];
for (let key in obj) {
    keys.push(key);
}
// Output: ["name", "age", "city"]
```
