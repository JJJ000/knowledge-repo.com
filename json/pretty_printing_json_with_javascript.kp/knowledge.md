---
title: Print json in a readable format using Javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use `JSON.stringify()` to pretty-print JSON using JavaScript.
---

**Contents**

[TOC]

### Using JSON.stringify()

`JSON.stringify()` is a JavaScript method that can be used to convert a JavaScript object into a string. This method can also be used to pretty-print JSON.

The syntax for `JSON.stringify()` is as follows:

```javascript
JSON.stringify(value[, replacer[, space]])
```

The `value` parameter is the JavaScript object that needs to be converted into a string. The `replacer` parameter is an optional parameter that can be used to modify the stringified object. The `space` parameter is an optional parameter that can be used to add whitespace to the output.

### Example

Here is an example of using `JSON.stringify()` to pretty-print a JavaScript object:

```javascript
let myObj = {
  name: "John",
  age: 30,
  hobbies: ["running", "reading", "cooking"]
};

let prettyPrintedObj = JSON.stringify(myObj, null, 2);

console.log(prettyPrintedObj);
```

The output of the code above will be:

```json
{
  "name": "John",
  "age": 30,
  "hobbies": [
    "running",
    "reading",
    "cooking"
  ]
}
```

### Using a Third-Party Library

Another way to pretty-print JSON is to use a third-party library such as json-formatter.

json-formatter is a JavaScript library that can be used to convert a JavaScript object into a string with proper indentation and line breaks.

The syntax for json-formatter is as follows:

```javascript
jsonFormatter.format(value)
```

The `value` parameter is the JavaScript object that needs to be converted into a string.

### Example

Here is an example of using json-formatter to pretty-print a JavaScript object:

```javascript
let myObj = {
  name: "John",
  age: 30,
  hobbies: ["running", "reading", "cooking"]
};

let prettyPrintedObj = jsonFormatter.format(myObj);

console.log(prettyPrintedObj);
```

The output of the code above will be:

```json
{
  "name": "John",
  "age": 30,
  "hobbies": [
    "running",
    "reading",
    "cooking"
  ]
}
```
