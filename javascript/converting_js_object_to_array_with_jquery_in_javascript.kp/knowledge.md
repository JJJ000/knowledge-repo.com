---
title: Transforming a js object into an array using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery`s $.map() method can be used to convert a JS object to an array.
---

**Contents**

[TOC]

#### Section 1 - Creating the Object

We can create a JavaScript object using the `Object` constructor or object literal notation.

Using the `Object` constructor:

```javascript
var obj = new Object();
obj.name = "John";
obj.age = 30;
```

Using object literal notation:

```javascript
var obj = {
  name: "John",
  age: 30
};
```

#### Section 2 - Converting Object to Array

We can use jQuery's `$.map()` function to convert the object to an array.

```javascript
var arr = $.map(obj, function(value, index) {
  return [value];
});
```

#### Section 3 - Output

The `arr` variable now contains an array with the values from the object:

```javascript
console.log(arr); // ["John", 30]
```

#### Section 4 - Iterating Over the Array

We can use a `for` loop to iterate over the array and access the values:

```javascript
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i]); // "John" and then 30
}
```
