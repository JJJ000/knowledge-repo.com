---
title: How can I create nicely formatted JSON from an object using javascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the JSON.stringify() method to generate formatted, easy-to-read JSON from an object.
---

**Contents**

[TOC]

## Using JSON.stringify

The JSON.stringify() method is the most commonly used method for generating formatted JSON from an object. It takes a JavaScript object as an argument, and returns a string representing the object in JSON format. The optional second argument allows you to specify the indentation level of the output.

## Example

For example, given the following object:

```javascript
let obj = {
  name: 'John',
  age: 30,
  isMarried: true
};
```

You can generate a formatted JSON string using JSON.stringify:

```javascript
let jsonString = JSON.stringify(obj, null, 2);

/*
{
  "name": "John",
  "age": 30,
  "isMarried": true
}
*/
```

## Other Options

There are other libraries available for generating formatted JSON from an object, such as jsonlint and json-formatter. These libraries provide more features and options than JSON.stringify, such as syntax highlighting and the ability to customize the output.
