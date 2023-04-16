---
title: What is the opposite of json.stringify?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JSON.parse is the reverse of JSON.stringify in Javascript.
---

**Contents**

[TOC]

### JSON.parse

JSON.parse() is the reverse of JSON.stringify() in Javascript. It takes a JSON string and parses it into an object, array, or other value.

### Syntax

The syntax for JSON.parse() is as follows:

```
JSON.parse(text[, reviver])
```

The `text` argument is a string containing the JSON data to be parsed. The optional `reviver` argument is a function that takes two arguments: `key` and `value`. It can be used to transform the results of JSON.parse().

### Example

The following example parses a JSON string and logs the parsed object to the console:

```
let jsonString = '{"name":"John","age":30,"city":"New York"}';
let jsonObj = JSON.parse(jsonString);
console.log(jsonObj);
```

This will log the following object to the console:

```
{
  name: "John",
  age: 30,
  city: "New York"
}
```

### Return Value

JSON.parse() returns the parsed value (object, array, string, number, boolean, or null). If the string cannot be parsed, it will return `undefined`.
