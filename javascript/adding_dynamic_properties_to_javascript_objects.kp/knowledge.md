---
title: Can you dynamically assign properties to a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Yes, it is possible to add dynamically named properties to JavaScript objects using bracket notation.
---

**Contents**

[TOC]

**Yes**

**Using Bracket Notation**

It is possible to add dynamically named properties to a JavaScript object using bracket notation. This allows you to create properties with names that are not known until runtime. 

For example:

```
var obj = {};
let key = 'name';
obj[key] = 'John';
console.log(obj.name); // John
```

**Using Object.defineProperty()**

It is also possible to add dynamically named properties to a JavaScript object using the Object.defineProperty() method. This allows you to create properties with names that are not known until runtime. 

For example:

```
var obj = {};
let key = 'name';
Object.defineProperty(obj, key, {
  value: 'John',
  writable: true,
  enumerable: true,
  configurable: true
});
console.log(obj.name); // John
```

**Using Object.defineProperties()**

It is also possible to add multiple dynamically named properties to a JavaScript object using the Object.defineProperties() method. This allows you to create properties with names that are not known until runtime. 

For example:

```
var obj = {};
let keys = {
  name: 'John',
  age: 25
};
Object.defineProperties(obj, keys);
console.log(obj.name); // John
console.log(obj.age); // 25
```
