---
title: What is the syntax for creating a JSON object with multiple arrays?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Create an object with multiple properties, each of which is an array of objects.
---

**Contents**

[TOC]

# Section 1: Creating the JSON Object 
A JSON object is created by using the following syntax: 
```
{
  "key1": "value1",
  "key2": "value2",
  ...
}
```

# Section 2: Adding Arrays
Arrays are added to the JSON object by using the following syntax: 
```
{
  "key1": "value1",
  "key2": [
    "value2",
    "value3",
    ...
  ],
  ...
}
```

# Section 3: Adding Multiple Arrays
Multiple arrays can be added to the JSON object by using the following syntax: 
```
{
  "key1": "value1",
  "key2": [
    "value2",
    "value3",
    ...
  ],
  "key3": [
    "value4",
    "value5",
    ...
  ],
  ...
}
```

# Section 4: Example
Here is an example of a JSON object with multiple arrays: 
```
{
  "name": "John Doe",
  "age": 30,
  "hobbies": [
    "reading",
    "cooking",
    "running"
  ],
  "friends": [
    "Jane Doe",
    "John Smith"
  ]
}
```
