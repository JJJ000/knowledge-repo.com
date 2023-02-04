---
title: What is the best way to access all of the values of a JavaScript object without knowing the keys?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Object.values() method to get an array of all the values of an object.
---

**Contents**

[TOC]

## Using for...in

The `for...in` loop is the most common way to iterate over the properties of an object in JavaScript.

```javascript
let obj = {
    prop1: "value1",
    prop2: "value2",
    prop3: "value3"
};

for (let key in obj) {
    console.log(obj[key]); // "value1", "value2", "value3"
}
```

## Using Object.values()

The `Object.values()` method returns an array of values of the given object.

```javascript
let obj = {
    prop1: "value1",
    prop2: "value2",
    prop3: "value3"
};

let values = Object.values(obj);
console.log(values); // ["value1", "value2", "value3"]
```

## Using Object.entries()

The `Object.entries()` method returns an array of key/value pairs of the given object.

```javascript
let obj = {
    prop1: "value1",
    prop2: "value2",
    prop3: "value3"
};

let entries = Object.entries(obj);
console.log(entries); // [["prop1", "value1"], ["prop2", "value2"], ["prop3", "value3"]]

// Iterate over entries
for (let [key, value] of entries) {
    console.log(value); // "value1", "value2", "value3"
}
```

## Using Object.getOwnPropertyNames()

The `Object.getOwnPropertyNames()` method returns an array of all properties (enumerable or not) found directly upon the given object.

```javascript
let obj = {
    prop1: "value1",
    prop2: "value2",
    prop3: "value3"
};

let props = Object.getOwnPropertyNames(obj);
console.log(props); // ["prop1", "prop2", "prop3"]

// Iterate over props
for (let key of props) {
    console.log(obj[key]); // "value1", "value2", "value3"
}
```
