---
title: What is the process for transforming a JSON object into a JavaScript array?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON.parse() method to convert a JSON object to a JavaScript array.
---

**Contents**

[TOC]

#### Section 1: Understand the JSON Object

JSON stands for JavaScript Object Notation and is a lightweight data-interchange format. It is used to store and exchange data between a server and a client. It is based on a subset of the JavaScript Programming Language and is easy to read and write.

#### Section 2: Convert JSON Object to JavaScript Array

JSON objects can be converted to JavaScript arrays using the `JSON.parse()` method. This method takes a JSON string and parses it into an array. The syntax for this method is `JSON.parse(text[, reviver])`. The `text` parameter is the JSON string that needs to be parsed and the `reviver` parameter is an optional parameter that can be used to transform the resulting array.

#### Section 3: Example

For example, consider the following JSON object: 

```
{
    "name": "John",
    "age": 30,
    "city": "New York"
}
```

This object can be converted to an array using the `JSON.parse()` method:

```
var obj = JSON.parse('{"name":"John","age":30,"city":"New York"}');
console.log(obj);
```

This will output the following array:

```
[
    "John",
    30,
    "New York"
]
```

#### Section 4: Conclusion

By using the `JSON.parse()` method, JSON objects can be easily converted to JavaScript arrays. This method can also be used to transform the resulting array by passing a `reviver` parameter.
