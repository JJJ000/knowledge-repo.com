---
title: What is the syntax for converting a string to JSON in node.js?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the built-in function JSON.parse() to convert a string to JSON.
---

**Contents**

[TOC]

1. Using `JSON.parse()` 

The `JSON.parse()` method parses a string as JSON and returns a JavaScript object.

```javascript
let jsonString = '{"name": "John", "age": 30}';
let jsonObject = JSON.parse(jsonString);

console.log(jsonObject.name); // John
console.log(jsonObject.age); // 30
```

2. Using `eval()`

The `eval()` function can also be used to convert a string to a JSON object.

```javascript
let jsonString = '{"name": "John", "age": 30}';
let jsonObject = eval('(' + jsonString + ')');

console.log(jsonObject.name); // John
console.log(jsonObject.age); // 30
```

3. Using `new Function()`

The `new Function()` constructor can also be used to convert a string to a JSON object.

```javascript
let jsonString = '{"name": "John", "age": 30}';
let jsonObject = new Function('return ' + jsonString)();

console.log(jsonObject.name); // John
console.log(jsonObject.age); // 30
```

4. Using `JSON5.parse()`

The `JSON5.parse()` method can also be used to convert a string to a JSON object. JSON5 is an extension of JSON that allows for the use of comments and other non-standard features.

```javascript
let jsonString = '{"name": "John", "age": 30}';
let jsonObject = JSON5.parse(jsonString);

console.log(jsonObject.name); // John
console.log(jsonObject.age); // 30
```
