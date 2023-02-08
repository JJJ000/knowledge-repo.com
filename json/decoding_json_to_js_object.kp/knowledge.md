---
title: Converting a JSON string into a JavaScript object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Deserializing a JSON into a JavaScript object involves parsing the JSON string into an object using the JSON.parse() method.
---

**Contents**

[TOC]

### Section 1: Creating an Object

To deserialize a JSON into a JavaScript object, we first need to create the object. This is done by using the `JSON.parse()` method, which takes a string containing the JSON object and returns an object.

### Section 2: Example

For example, if we have the following JSON object:

```
{
    "name": "John Doe",
    "age": 32
}
```

We can create a JavaScript object by using the following code:

```javascript
const jsonString = '{"name": "John Doe", "age": 32}';
const object = JSON.parse(jsonString);
```

### Section 3: Accessing Properties

Once we have created the object, we can access the properties of the object using dot notation. For example, to access the name property of the object, we can use the following code:

```javascript
const name = object.name; // "John Doe"
```

### Section 4: Working with Arrays

If the JSON contains an array, we can access the elements of the array using the `[]` syntax. For example, if we have the following JSON object:

```
{
    "name": "John Doe",
    "age": 32,
    "hobbies": ["fishing", "hiking", "swimming"]
}
```

We can access the first element of the hobbies array using the following code:

```javascript
const firstHobby = object.hobbies[0]; // "fishing"
```
