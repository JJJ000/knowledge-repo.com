---
title: How can Javascript be used to process json data?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-14 00:00:00
updated_at: 2023-01-14 00:00:00
tldr: JSON can be parsed in JavaScript using the built-in `JSON.parse()` method.
---

**Contents**

[TOC]

### Using JSON.parse()
`JSON.parse()` is a built-in method in JavaScript that parses a JSON string and returns the JavaScript object.

Syntax:
```javascript
JSON.parse(text[, reviver]);
```

Example:
```javascript
var jsonString = '{"name":"John", "age":30, "city":"New York"}';
var jsonObj = JSON.parse(jsonString);
console.log(jsonObj.name); // Output: John
```

### Using eval()
The JavaScript `eval()` function is used to evaluate a string as JavaScript code.

Syntax:
```javascript
eval(string);
```

Example:
```javascript
var jsonString = '{"name":"John", "age":30, "city":"New York"}';
var jsonObj = eval("(" + jsonString + ")");
console.log(jsonObj.name); // Output: John
```
