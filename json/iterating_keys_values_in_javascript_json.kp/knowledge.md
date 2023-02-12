---
title: How can I loop through the keys and values of a JSON object in javascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can use a `for...in` loop to iterate through the keys and values of a JSON object.
---

**Contents**

[TOC]

## Using For Loop

```javascript
var json = {
  "name": "John",
  "age": 30,
  "city": "New York"
};

for (var key in json) {
  if (json.hasOwnProperty(key)) {
    console.log("key: " + key + ", value: " + json[key]);
  }
}
```

## Using Object.keys()

```javascript
var json = {
  "name": "John",
  "age": 30,
  "city": "New York"
};

Object.keys(json).forEach(function(key) {
  console.log("key: " + key + ", value: " + json[key]);
});
```

## Using Object.entries()

```javascript
var json = {
  "name": "John",
  "age": 30,
  "city": "New York"
};

Object.entries(json).forEach(([key, value]) => {
  console.log("key: " + key + ", value: " + value);
});
```

## Using forEach()

```javascript
var json = {
  "name": "John",
  "age": 30,
  "city": "New York"
};

Object.keys(json).forEach(key => {
  console.log("key: " + key + ", value: " + json[key]);
});
```
