---
title: Determine if a key is present in a JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, you can use the hasOwnProperty() method to check if a key exists inside a JSON object.
---

**Contents**

[TOC]

#### Using the `hasOwnProperty()` Method

The `hasOwnProperty()` method is used to check if a key exists inside a JSON object.

Syntax:
```
jsonObject.hasOwnProperty(key);
```

Example:
```
let jsonObject = {
  name: "John",
  age: 30
};

jsonObject.hasOwnProperty("name"); // true
jsonObject.hasOwnProperty("address"); // false
```

#### Using the `in` Operator

The `in` operator is used to check if a key exists inside a JSON object.

Syntax:
```
key in jsonObject
```

Example:
```
let jsonObject = {
  name: "John",
  age: 30
};

"name" in jsonObject; // true
"address" in jsonObject; // false
```

#### Using the `Object.keys()` Method

The `Object.keys()` method is used to get an array of the keys of a JSON object. We can then use `Array.prototype.includes()` to check if a key exists inside the JSON object.

Syntax:
```
Object.keys(jsonObject).includes(key);
```

Example:
```
let jsonObject = {
  name: "John",
  age: 30
};

Object.keys(jsonObject).includes("name"); // true
Object.keys(jsonObject).includes("address"); // false
```
