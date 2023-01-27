---
title: What is the most efficient way to combine the attributes of two JavaScript objects?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the Object.assign() method to merge the properties of two JavaScript objects dynamically.
---

**Contents**

[TOC]

### 1. Using Object.assign()

Object.assign() can be used to merge two or more objects together. This method takes the target object as the first argument, followed by one or more source objects. The properties of the source objects will be copied to the target object.

```
const target = {};

const source1 = {
  name: 'John',
  age: 25
};

const source2 = {
  address: 'New York City'
};

Object.assign(target, source1, source2);

console.log(target); // { name: 'John', age: 25, address: 'New York City' }
```

### 2. Using Spread Operator

The spread operator (...) can also be used to merge two or more objects together. This method takes the target object as the first argument, followed by one or more source objects. The properties of the source objects will be copied to the target object.

```
const target = {};

const source1 = {
  name: 'John',
  age: 25
};

const source2 = {
  address: 'New York City'
};

const merged = { ...target, ...source1, ...source2 };

console.log(merged); // { name: 'John', age: 25, address: 'New York City' }
```

### 3. Using Object.keys() and for..in loop

Object.keys() and a for..in loop can also be used to merge two or more objects together. This method takes the target object and one or more source objects. The properties of the source objects will be copied to the target object.

```
const target = {};

const source1 = {
  name: 'John',
  age: 25
};

const source2 = {
  address: 'New York City'
};

const sources = [source1, source2];

for (let i = 0; i < sources.length; i++) {
  const source = sources[i];
  const keys = Object.keys(source);
  for (let j = 0; j < keys.length; j++) {
    const key = keys[j];
    target[key] = source[key];
  }
}

console.log(target); // { name: 'John', age: 25, address: 'New York City' }
```

### 4. Using Lodash's merge()

Lodash's merge() method can be used to merge two or more objects together. This method takes the target object as the first argument, followed by one or more source objects. The properties of the source objects will be copied to the target object.

```
const target = {};

const source1 = {
  name: 'John',
  age: 25
};

const source2 = {
  address: 'New York City'
};

const merged = _.merge(target, source1, source2);

console.log(merged); // { name: 'John', age: 25, address: 'New York City' }
```
