---
title: Transform a Javascript object into a json string
authors:
- cool_wizard
tags:
- javascript
- json
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-15 00:00:00
updated_at: 2023-01-15 00:00:00
tldr: Use the `JSON.stringify()` method to convert a JavaScript object to a JSON string.
---

**Contents**

[TOC]

### What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and objects.

### What is a JS Object?
A JavaScript object is an unordered collection of key-value pairs. It is similar to a Dictionary or Hashtable in other programming languages.

### How to Convert JS Object to JSON String
The process of converting a JS object to a JSON string is known as serialization. To serialize a JS object, you can use the JSON.stringify() method. This method takes the object as an argument and returns a JSON string.

### Example
For example, let's say we have a JS object as follows:

```javascript
let object = {
  name: 'John',
  age: 30
};
```

To convert this object to a JSON string, we can use the `JSON.stringify()` method:

```javascript
let jsonString = JSON.stringify(object);
```

The resulting JSON string will look like this:

```javascript
{"name":"John","age":30}
```
