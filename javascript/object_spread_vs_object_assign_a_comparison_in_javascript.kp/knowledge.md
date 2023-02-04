---
title: Comparing the differences between using object spread syntax and object.assign() to copy properties from one object to another
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Object spread allows for a more concise and intuitive syntax for copying enumerable properties from one object to another, while Object.assign() copies the values of all enumerable own properties from one or more source objects to a target object.
---

**Contents**

[TOC]

### Object Spread
Object spread is a syntax introduced in ES2018 that allows for the spreading of objects. It allows for the copying of all properties from one object to another. The syntax looks like this:

```
let obj1 = { a: 1, b: 2 };
let obj2 = { ...obj1, c: 3 };

console.log(obj2); // { a: 1, b: 2, c: 3 }
```

Object spread is useful for copying the properties of one object to another without mutating the original object. It also allows for the merging of multiple objects into one.

### Object.assign
Object.assign is a method introduced in ES2015 that allows for the merging of two or more objects into one. It is used to copy the properties of one object to another. The syntax looks like this:

```
let obj1 = { a: 1, b: 2 };
let obj2 = { c: 3 };

let obj3 = Object.assign(obj1, obj2);

console.log(obj3); // { a: 1, b: 2, c: 3 }
```

Object.assign is useful for copying the properties of one object to another without mutating the original object. It also allows for the merging of multiple objects into one.
