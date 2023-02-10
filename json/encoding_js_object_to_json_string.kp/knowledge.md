---
title: Converting a JavaScript object into a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON.stringify() method to encode a Javascript object into a JSON string.
---

**Contents**

[TOC]

#### Using JSON.stringify()

The JSON.stringify() method is used to convert a JavaScript object or value to a JSON string.

Syntax:
```
JSON.stringify(value[, replacer[, space]])
```

Example:
```
var person = {
  firstName: "John",
  lastName: "Doe"
};

var jsonString = JSON.stringify(person);
console.log(jsonString);

// Output: {"firstName":"John","lastName":"Doe"}
```

#### Using for..in loop

The for..in loop is used to iterate over the properties of an object.

Syntax:
```
for (var property in object) {
  // statement
}
```

Example:
```
var person = {
  firstName: "John",
  lastName: "Doe"
};

var jsonString = "{";

for (var property in person) {
  jsonString += '"' + property + '":"' + person[property] + '",';
}

// Remove the trailing comma
jsonString = jsonString.slice(0, -1);

jsonString += "}";

console.log(jsonString);

// Output: {"firstName":"John","lastName":"Doe"}
```
