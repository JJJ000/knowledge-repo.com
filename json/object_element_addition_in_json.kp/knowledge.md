---
title: Incorporating items into an object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can add elements to a JSON object by using the dot notation or bracket notation.
---

**Contents**

[TOC]

#### Adding a New Key-Value Pair

Adding a new key-value pair to a JSON object is as simple as defining a new property on the object and assigning it a value.

```javascript
let jsonObject = {
  "name": "John Doe"
};

jsonObject.age = 25;
```

#### Adding an Element to an Array

If the value of a key in a JSON object is an array, you can add a new element to the array by using the `push()` method.

```javascript
let jsonObject = {
  "name": "John Doe",
  "hobbies": ["hiking", "reading"]
};

jsonObject.hobbies.push("swimming");
```

#### Adding a Nested Object

You can add a nested object to a JSON object by defining a new property and assigning it an object.

```javascript
let jsonObject = {
  "name": "John Doe"
};

jsonObject.address = {
  "street": "123 Main St",
  "city": "Anytown",
  "state": "CA"
};
```

#### Adding a Nested Array

You can add a nested array to a JSON object by defining a new property and assigning it an array.

```javascript
let jsonObject = {
  "name": "John Doe"
};

jsonObject.favoriteBooks = ["The Great Gatsby", "The Catcher in the Rye", "To Kill a Mockingbird"];
```
