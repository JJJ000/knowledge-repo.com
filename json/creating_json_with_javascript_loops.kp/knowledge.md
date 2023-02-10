---
title: What is the syntax for using a JavaScript for loop to generate a JSON object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can create a JSON object by looping through an array and adding each element as a key-value pair.
---

**Contents**

[TOC]

## Section 1: Create empty array

To create a JSON object with JavaScript, we need to start by creating an empty array. This array will be populated with the data we want to store in our JSON object.

```javascript
var jsonArray = [];
```

## Section 2: Populate the array using a for loop

Once we have our empty array, we can use a for loop to populate it with the data we want to store. The code below shows an example of a for loop that adds three elements to the array.

```javascript
for (var i = 0; i < 3; i++) {
  jsonArray.push({
    "key": i,
    "value": "Some value"
  });
}
```

## Section 3: Convert the array to a JSON object

Once we have populated our array with the data we want to store, we can use the `JSON.stringify()` method to convert it to a JSON object.

```javascript
var jsonObject = JSON.stringify(jsonArray);
```

## Section 4: Output the JSON object

Finally, we can output the JSON object to the console or a file.

```javascript
console.log(jsonObject);
```
