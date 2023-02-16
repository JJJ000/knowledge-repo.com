---
title: Transform map into a JavaScript object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: A Map can be converted to a JavaScript object by using the JSON.stringify() method.
---

**Contents**

[TOC]

# Section 1: Map to JSON

Converting a Map to a JSON object is a relatively straightforward process. The Map object can be iterated over and each key-value pair can be added to a new JSON object. The keys of the Map object can be used as the keys of the JSON object, and the values of the Map object can be used as the values of the JSON object.

# Section 2: Iterating Over the Map

In order to convert a Map to a JSON object, the Map must first be iterated over. This can be done using a for...of loop, which will iterate over each key-value pair in the Map. The key-value pairs can then be added to a new JSON object.

# Section 3: Adding Key-Value Pairs to JSON

Once the Map has been iterated over, the key-value pairs can be added to the new JSON object. This can be done using the set() method, which takes two arguments: the key and the value. The key should be the key of the Map object, and the value should be the value of the Map object.

# Section 4: Example

Below is an example of how to convert a Map to a JSON object.

```
let myMap = new Map();
myMap.set('name', 'John');
myMap.set('age', 30);

let jsonObj = {};
for (let [key, value] of myMap) {
  jsonObj[key] = value;
}

console.log(jsonObj); // { name: 'John', age: 30 }
```
