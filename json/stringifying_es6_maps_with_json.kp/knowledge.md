---
title: What is the process for converting an es6 map into a JSON string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the `JSON.stringify()` method to convert an ES6 Map to JSON.
---

**Contents**

[TOC]

#### Step 1: Convert Map to Array

The first step is to convert the ES6 Map to an array. This can be done by using the `Array.from()` method.

```javascript
let map = new Map();
map.set('name', 'John');
map.set('age', 25);

let arr = Array.from(map);
```

#### Step 2: Convert Array to JSON

Once the Map is converted to an array, we can use the `JSON.stringify()` method to convert it to a JSON string.

```javascript
let jsonString = JSON.stringify(arr);
```

#### Step 3: Parse JSON

The final step is to parse the JSON string to get the key-value pairs. This can be done using the `JSON.parse()` method.

```javascript
let parsedJSON = JSON.parse(jsonString);
```

#### Step 4: Access Key-Value Pairs

Finally, the key-value pairs can be accessed by iterating through the parsed JSON object.

```javascript
for (let key in parsedJSON) {
  let value = parsedJSON[key];
  console.log(key + ': ' + value);
}
```
