---
title: Create a new property on a JSON object using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the dot notation or the bracket notation to add a new attribute (element) to a JSON object using JavaScript.
---

**Contents**

[TOC]

## Section 1: Create the JSON Object

We can create a JSON object using JavaScript with the following code:

```javascript
let myJSONObject = {
    "name": "John Doe",
    "age": 25
};
```

## Section 2: Add Attribute

To add a new attribute to the JSON object, we can use the following code:

```javascript
myJSONObject["occupation"] = "Software Engineer";
```

## Section 3: Verifying the Result

We can verify the result by logging the JSON object to the console:

```javascript
console.log(myJSONObject);
```

The output should be:

```javascript
{
  "name": "John Doe",
  "age": 25,
  "occupation": "Software Engineer"
}
```

## Section 4: Stringify the JSON Object

If we need to convert the JSON object to a string, we can use the `JSON.stringify()` method:

```javascript
let myJSONString = JSON.stringify(myJSONObject);
console.log(myJSONString);
```

The output should be:

```javascript
{"name":"John Doe","age":25,"occupation":"Software Engineer"}
```
