---
title: Yaml representation of an array of objects in json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The YAML equivalent of an array of objects in JSON is a list of mappings.
---

**Contents**

[TOC]

#### Section 1: Defining an Array of Objects in JSON

An array of objects in JSON is an array of key-value pairs, where each key-value pair is an object. Each object in the array can have its own set of keys and values.

For example, let's say we have an array of objects that contains information about people:

```
[
  {
    "name": "John",
    "age": 25,
    "gender": "male"
  },
  {
    "name": "Jane",
    "age": 30,
    "gender": "female"
  }
]
```

#### Section 2: Defining an Array of Objects in YAML

An array of objects in YAML is defined in a similar way as an array of objects in JSON. However, YAML uses a different syntax.

For example, the same array of people from above could be defined in YAML like this:

```
- name: John
  age: 25
  gender: male
- name: Jane
  age: 30
  gender: female
```

#### Section 3: Advantages of YAML

YAML is a more human-readable format than JSON. It is easier to read and understand, and it also allows for comments in the code. This makes it easier to debug and maintain.

#### Section 4: Disadvantages of YAML

The main disadvantage of YAML is that it is not as widely supported as JSON. While most programming languages support JSON, not all of them support YAML. Additionally, YAML is not as compact as JSON, which can make it more difficult to parse and process.
