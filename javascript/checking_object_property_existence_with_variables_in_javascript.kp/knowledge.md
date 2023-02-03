---
title: What is the best way to determine if an object has a property whose name is stored in a variable?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the `in` operator to check if an object property exists with a variable holding the property name.
---

**Contents**

[TOC]

## Using the `in` Operator

The `in` operator can be used to check if an object has a property with a given name. This operator returns true if the specified property is in the object, and false if not.

```js
let obj = {
  prop1: "value1",
  prop2: "value2"
};

let propName = "prop1";

if (propName in obj) {
  console.log("Object has the given property");
} else {
  console.log("Object does not have the given property");
}
```

## Using the `hasOwnProperty()` Method

The `hasOwnProperty()` method can be used to check if an object has a property with a given name. This method returns true if the specified property is in the object, and false if not.

```js
let obj = {
  prop1: "value1",
  prop2: "value2"
};

let propName = "prop1";

if (obj.hasOwnProperty(propName)) {
  console.log("Object has the given property");
} else {
  console.log("Object does not have the given property");
}
```

## Using the `Object.keys()` Method

The `Object.keys()` method can be used to check if an object has a property with a given name. This method returns an array of all the properties in the object, and the array can then be searched to see if the specified property is in it.

```js
let obj = {
  prop1: "value1",
  prop2: "value2"
};

let propName = "prop1";

let keys = Object.keys(obj);

if (keys.indexOf(propName) > -1) {
  console.log("Object has the given property");
} else {
  console.log("Object does not have the given property");
}
```
