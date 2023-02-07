---
title: See if a key is present in a JSON object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the `in` operator to check if a key exists inside a JSON object in Javascript.
---

**Contents**

[TOC]

**1. Using the `in` Operator**

The `in` operator can be used to check if a key exists in a JSON object. It returns a boolean value of `true` if the key exists, and `false` if it does not.

```javascript
const object = {
    key1: 'value1',
    key2: 'value2'
};

const keyExists = 'key1' in object; // returns true
const keyDoesNotExist = 'key3' in object; // returns false
```

**2. Using the `hasOwnProperty()` Method**

The `hasOwnProperty()` method can also be used to check if a key exists in a JSON object. It also returns a boolean value of `true` if the key exists, and `false` if it does not.

```javascript
const object = {
    key1: 'value1',
    key2: 'value2'
};

const keyExists = object.hasOwnProperty('key1'); // returns true
const keyDoesNotExist = object.hasOwnProperty('key3'); // returns false
```

**3. Using the `Object.keys()` Method**

The `Object.keys()` method can be used to return an array of all the keys in a JSON object. This array can then be used to check if a key exists in the object.

```javascript
const object = {
    key1: 'value1',
    key2: 'value2'
};

const keys = Object.keys(object); // returns ['key1', 'key2']
const keyExists = keys.includes('key1'); // returns true
const keyDoesNotExist = keys.includes('key3'); // returns false
```

**4. Using the `Object.entries()` Method**

The `Object.entries()` method can be used to return an array of all the key-value pairs in a JSON object. This array can then be used to check if a key exists in the object.

```javascript
const object = {
    key1: 'value1',
    key2: 'value2'
};

const entries = Object.entries(object); // returns [['key1', 'value1'], ['key2', 'value2']]
const keyExists = entries.some(entry => entry[0] === 'key1'); // returns true
const keyDoesNotExist = entries.some(entry => entry[0] === 'key3'); // returns false
```
