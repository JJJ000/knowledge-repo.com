---
title: Creating a copy of an object using typescript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To clone an object in JavaScript, use the Object.assign() method or the spread operator (...).
---

**Contents**

[TOC]

## Deep Cloning
Deep cloning is a process of creating an exact copy of an object or array while preserving its original structure and data. This is done by recursively looping through the object's properties and creating a new object with the same values. In TypeScript, this can be done with the spread operator (`...`).

```typescript
let originalObject = {
  a: 1,
  b: 'Hello',
  c: {
    x: 10,
    y: 20
  }
};

let clonedObject = {...originalObject};
```

## Shallow Cloning
Shallow cloning is a process of creating an exact copy of an object or array while preserving its original structure, but not its data. This is done by creating a new object with the same keys and values as the original object. In TypeScript, this can be done with the Object.assign() method.

```typescript
let originalObject = {
  a: 1,
  b: 'Hello',
  c: {
    x: 10,
    y: 20
  }
};

let clonedObject = Object.assign({}, originalObject);
```

## JSON.parse() and JSON.stringify()
JSON.parse() and JSON.stringify() are two methods that can be used to clone an object in TypeScript. The JSON.stringify() method converts a JavaScript object into a JSON string, while the JSON.parse() method converts a JSON string into a JavaScript object.

```typescript
let originalObject = {
  a: 1,
  b: 'Hello',
  c: {
    x: 10,
    y: 20
  }
};

let clonedObject = JSON.parse(JSON.stringify(originalObject));
```

## Lodash _.cloneDeep()
Lodash is a JavaScript library that provides utility functions for common programming tasks. The _.cloneDeep() method is a utility function that can be used to clone an object in TypeScript. The _.cloneDeep() method performs a deep cloning of the object, preserving its original structure and data.

```typescript
import * as _ from 'lodash';

let originalObject = {
  a: 1,
  b: 'Hello',
  c: {
    x: 10,
    y: 20
  }
};

let clonedObject = _.cloneDeep(originalObject);
```
