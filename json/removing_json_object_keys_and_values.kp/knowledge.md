---
title: What is the process for deleting a key and its associated value from a JSON object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the delete operator to remove a key and its associated value from a JSON object.
---

**Contents**

[TOC]

### Option 1: Using delete

The `delete` operator can be used to remove a key and its associated value from a JSON object.

```javascript
let jsonObj = {
  key1: "value1",
  key2: "value2"
};

delete jsonObj.key1;

console.log(jsonObj); // { key2: "value2" }
```

### Option 2: Using Object.assign

The `Object.assign()` method can be used to create a new object by copying the values of existing objects, excluding the specified key and its associated value.

```javascript
let jsonObj = {
  key1: "value1",
  key2: "value2"
};

let newObj = Object.assign({}, jsonObj);
delete newObj.key1;

console.log(newObj); // { key2: "value2" }
```

### Option 3: Using Lodash

The `_.omit()` method from the Lodash library can be used to create a new object by copying the values of an existing object, excluding the specified key and its associated value.

```javascript
let jsonObj = {
  key1: "value1",
  key2: "value2"
};

let newObj = _.omit(jsonObj, 'key1');

console.log(newObj); // { key2: "value2" }
```

### Option 4: Using Spread Operator

The spread operator (`...`) can be used to create a new object by copying the values of an existing object, excluding the specified key and its associated value.

```javascript
let jsonObj = {
  key1: "value1",
  key2: "value2"
};

let { key1, ...newObj } = jsonObj;

console.log(newObj); // { key2: "value2" }
```
