---
title: What is the syntax for accessing a jsonarray without a name?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: It is not possible to get a JSONArray without an array name in JSON.
---

**Contents**

[TOC]

### Section 1: What is a JSONArray?
A JSONArray is an ordered collection of values, similar to an array in other programming languages. Each value in the array is an object, and can be any valid JSON data type, such as a string, number, boolean, or another array.

### Section 2: How to Access a JSONArray
A JSONArray can be accessed using the same methods used to access objects in JSON, such as bracket notation, dot notation, and the get() method.

### Section 3: How to Get a JSONArray Without an Array Name
To get a JSONArray without an array name, you can use the JSON.parse() method to parse the JSON string. This will return the entire array as an object, which can then be accessed using the same methods used to access objects in JSON.

### Section 4: Example
For example, if you have the following JSON string:

```
[
   {
      "name":"John",
      "age":30
   },
   {
      "name":"Tom",
      "age":25
   }
]
```

You can use the JSON.parse() method to parse the string and return the array as an object:

```
let jsonArray = JSON.parse('[{"name":"John","age":30},{"name":"Tom","age":25}]');
```

You can then access the array using the same methods used to access objects in JSON, such as bracket notation, dot notation, and the get() method.
