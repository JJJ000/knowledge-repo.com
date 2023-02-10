---
title: Transform string into a JSON array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: A string can be converted to a JSON array by using the JSON.parse() method.
---

**Contents**

[TOC]

# Section 1: Understanding JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is a text-based, human-readable format that is used to represent data structures and objects. JSON is often used to serialize and transfer data over a network connection, such as between a web server and a client.

# Section 2: Converting a String to a JSON Array

A JSON array is a collection of values that are enclosed within square brackets and separated by commas. To convert a string to a JSON array, the string must first be parsed into a JavaScript object. This can be done using the JSON.parse() method, which takes a JSON string and parses it into a JavaScript object.

# Section 3: Example

For example, if we have the following string:

```
var str = "{name: 'John', age: 30}";
```

We can convert it to a JSON array by using the JSON.parse() method:

```
var obj = JSON.parse(str);
```

This will result in the following JSON array:

```
[
    {
        "name": "John",
        "age": 30
    }
]
```

# Section 4: Conclusion

In conclusion, it is possible to convert a string to a JSON array by using the JSON.parse() method. This method takes a JSON string and parses it into a JavaScript object, which can then be converted into a JSON array.
