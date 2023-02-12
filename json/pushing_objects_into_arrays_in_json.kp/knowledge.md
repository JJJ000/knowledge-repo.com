---
title: What is the best way to add an object to an array?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the Array.push() method to add an object to an array in JSON.
---

**Contents**

[TOC]

### Create an Array

Create an array in JSON format by using the `[]` syntax. For example, to create an array of strings:

```json
["apple", "banana", "cherry"]
```

### Push an Object

To push an object into an array, you can use the `push()` method. For example, to push an object with two properties into the array:

```json
["apple", "banana", "cherry"].push({
  "name": "orange",
  "color": "orange"
});
```

### Result

The result of the above code is an array with four elements:

```json
["apple", "banana", "cherry", {
  "name": "orange",
  "color": "orange"
}]
```

### Alternative

Alternatively, you can also use the `concat()` method to add objects to an array. For example:

```json
["apple", "banana", "cherry"].concat({
  "name": "orange",
  "color": "orange"
});
```

The result of the above code is the same as using the `push()` method.
