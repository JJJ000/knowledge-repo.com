---
title: Retrieve the properties of a JSON object in javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the Object.keys() method to get the keys of a JSON object.
---

**Contents**

[TOC]

# Using Object.keys()

Object.keys() is a built-in JavaScript method that returns an array of the keys of an object.

## Syntax

```
Object.keys(object)
```

## Example

```
let person = {
  name: 'John',
  age: 30
};

let keys = Object.keys(person);
console.log(keys);
// Output: ['name', 'age']
```

# Using for...in loop

for...in is a looping statement that iterates over the properties of an object.

## Syntax

```
for (let key in object) {
  // code to be executed
}
```

## Example

```
let person = {
  name: 'John',
  age: 30
};

let keys = [];

for (let key in person) {
  keys.push(key);
}

console.log(keys);
// Output: ['name', 'age']
```
