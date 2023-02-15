---
title: Transform a JSON string into an array of JSON objects using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: JSON.parse() can be used to convert a JSON string to an array of JSON objects in Javascript.
---

**Contents**

[TOC]

# Section 1 - Parse JSON String

To convert a JSON string to an array of JSON objects, we can use the `JSON.parse()` method. This method takes a JSON string as an argument and returns a JavaScript object.

```javascript
let jsonString = '[{"name":"John","age":30},{"name":"Mary","age":25}]';

let jsonObjects = JSON.parse(jsonString);
```

# Section 2 - Access JSON Objects

Once the JSON string has been parsed, we can access the individual objects in the array. To do this, we can use the `forEach()` method to loop through the array and access each object.

```javascript
jsonObjects.forEach(function(jsonObject) {
  console.log(jsonObject.name);
  console.log(jsonObject.age);
});
```

# Section 3 - Modify JSON Objects

We can also modify the JSON objects in the array. To do this, we can use the `map()` method to loop through the array and modify each object.

```javascript
let modifiedJsonObjects = jsonObjects.map(function(jsonObject) {
  jsonObject.name = jsonObject.name + ' Smith';
  return jsonObject;
});
```

# Section 4 - Stringify JSON Objects

Finally, we can convert the array of JSON objects back into a JSON string. To do this, we can use the `JSON.stringify()` method. This method takes a JavaScript object as an argument and returns a JSON string.

```javascript
let modifiedJsonString = JSON.stringify(modifiedJsonObjects);
```
