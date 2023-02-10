---
title: The push() method of JavaScript objects
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The push() function is used to add one or more elements to the end of a JavaScript Object.
---

**Contents**

[TOC]

# What is push()?

The push() method is used to add one or more elements to the end of an array. It modifies the array on which it is invoked and returns the new length of the array.

# Syntax

array.push(element1[, ...[, elementN]])

# Example

```
var array = [1, 2, 3];
array.push(4);
console.log(array);
// Output: [1, 2, 3, 4]
```

# How it works in JSON?

JSON objects are written in key/value pairs. The push() method can be used to add a new key/value pair to the end of a JSON object. 

For example, if you have a JSON object like this:

```
{
    "name": "John Doe",
    "age": 30
}
```

You can use the push() method to add a new key/value pair like this:

```
var jsonObject = {
    "name": "John Doe",
    "age": 30
};

jsonObject.push({"gender": "male"});

console.log(jsonObject);
// Output: { "name": "John Doe", "age": 30, "gender": "male" }
```
