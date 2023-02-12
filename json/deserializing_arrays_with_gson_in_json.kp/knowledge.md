---
title: Converting a JSON string into a collection of objects that contain arrays
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Gson can be used to deserialize an array of objects with arrays in it from Json by using the fromJson() method.
---

**Contents**

[TOC]

# Section 1: Overview
Gson is a Java library that can be used to convert Java objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object. Gson can work with arbitrary Java objects including pre-existing objects that you do not have source-code of.

# Section 2: Deserializing an Array of Objects with Arrays
When deserializing an array of objects with arrays in it, Gson will create an array of objects from the JSON string. Each element in the array will be an object with the properties from the JSON string. This means that the properties in the JSON string will be mapped to the fields of the objects in the array.

# Section 3: Example
For example, given the following JSON string:

```
[
  {
    "name": "John",
    "age": 20,
    "hobbies": [
      "reading",
      "swimming"
    ]
  },
  {
    "name": "Jane",
    "age": 22,
    "hobbies": [
      "cooking",
      "dancing"
    ]
  }
]
```

Gson will create an array of two objects, each with the properties `name`, `age`, and `hobbies`. The `hobbies` property will be an array containing the elements from the JSON string.

# Section 4: Conclusion
In conclusion, Gson can be used to deserialize an array of objects with arrays in it. It will map the properties from the JSON string to the fields of the objects in the array, and will create an array for any properties that are arrays in the JSON string.
