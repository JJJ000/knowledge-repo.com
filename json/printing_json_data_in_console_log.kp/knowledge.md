---
title: What is the syntax for outputting JSON data to the console?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use console.log(JSON.stringify(data)) to print JSON data in the console.
---

**Contents**

[TOC]

# 1. Parse JSON into a JavaScript Object

To print JSON data in console.log, the first step is to parse the JSON string into a JavaScript object. This can be done using the JSON.parse() method.

```javascript
var jsonData = '{"name":"John", "age":30, "city":"New York"}';
var jsObject = JSON.parse(jsonData);
```

# 2. Log the JavaScript Object

Once the JSON string has been parsed into a JavaScript object, it can be logged to the console using the console.log() method.

```javascript
console.log(jsObject);
```

# 3. Output the Data

The JavaScript object can also be outputted to the console using the console.dir() method. This will output the data in a more readable format.

```javascript
console.dir(jsObject);
```

# 4. Stringify the Data

If the data needs to be outputted as a JSON string, the JSON.stringify() method can be used.

```javascript
var jsonString = JSON.stringify(jsObject);
console.log(jsonString);
```
