---
title: Take out a JSON attribute
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: To remove an attribute from a JSON object, use the delete operator.
---

**Contents**

[TOC]

**Removing a JSON Attribute**

**Method 1: Using the delete Operator**

1. Access the JSON object using the dot notation or the bracket notation.
2. Use the delete operator to delete the attribute.

**Example**

```
let person = {
    name: "John",
    age: 30,
    city: "New York"
};

delete person.city;

console.log(person);

// Output: {name: "John", age: 30}
```

**Method 2: Using the Splice Method**

1. Access the JSON object using the dot notation or the bracket notation.
2. Use the splice method to delete the attribute.

**Example**

```
let person = {
    name: "John",
    age: 30,
    city: "New York"
};

person.splice("city", 1);

console.log(person);

// Output: {name: "John", age: 30}
```
