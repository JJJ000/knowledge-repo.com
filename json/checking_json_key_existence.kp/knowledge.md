---
title: What is the process for determining if a JSON key is present?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the `hasOwnProperty()` method to check if a JSON key exists in a JSON object.
---

**Contents**

[TOC]

# Section 1: Using the `in` Operator

The `in` operator can be used to check if a key exists in a JSON object. This operator will return `true` if the specified key is present in the JSON object and `false` if it is not.

Example:

```javascript
let jsonObject = {
  "name": "John Doe",
  "age": 30
};

let key = "name";

if (key in jsonObject) {
  console.log("Key exists!");
} else {
  console.log("Key does not exist!");
}
```

# Section 2: Using the `hasOwnProperty()` Method

The `hasOwnProperty()` method can be used to check if a key exists in a JSON object. This method will return `true` if the specified key is present in the JSON object and `false` if it is not.

Example:

```javascript
let jsonObject = {
  "name": "John Doe",
  "age": 30
};

let key = "name";

if (jsonObject.hasOwnProperty(key)) {
  console.log("Key exists!");
} else {
  console.log("Key does not exist!");
}
```

# Section 3: Using the `Object.keys()` Method

The `Object.keys()` method can be used to check if a key exists in a JSON object. This method will return an array of keys present in the JSON object.

Example:

```javascript
let jsonObject = {
  "name": "John Doe",
  "age": 30
};

let key = "name";

if (Object.keys(jsonObject).includes(key)) {
  console.log("Key exists!");
} else {
  console.log("Key does not exist!");
}
```

# Section 4: Using the `Object.getOwnPropertyNames()` Method

The `Object.getOwnPropertyNames()` method can be used to check if a key exists in a JSON object. This method will return an array of keys present in the JSON object.

Example:

```javascript
let jsonObject = {
  "name": "John Doe",
  "age": 30
};

let key = "name";

if (Object.getOwnPropertyNames(jsonObject).includes(key)) {
  console.log("Key exists!");
} else {
  console.log("Key does not exist!");
}
```
