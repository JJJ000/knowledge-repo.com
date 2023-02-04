---
title: What is the best way to loop through a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use a for-in loop to iterate over a JavaScript object.
---

**Contents**

[TOC]

#### For-in Loop

The most common way to iterate over a JavaScript object is to use a `for-in` loop. This loop will iterate over all the enumerable properties of an object.

```javascript
for (const key in object) {
  console.log(key, object[key]);
}
```

#### Object.keys

Another way to iterate over an object is to use the `Object.keys()` method. This method will return an array of the object's own enumerable properties.

```javascript
Object.keys(object).forEach(key => {
  console.log(key, object[key]);
});
```

#### Object.entries

The `Object.entries()` method can also be used to iterate over an object. This method will return an array of arrays, each containing a key-value pair.

```javascript
Object.entries(object).forEach(([key, value]) => {
  console.log(key, value);
});
```

#### Object.values

The `Object.values()` method can also be used to iterate over an object. This method will return an array of the object's own enumerable property values.

```javascript
Object.values(object).forEach(value => {
  console.log(value);
});
```
