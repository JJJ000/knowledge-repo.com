---
title: Structure of a list of objects in JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: A list of objects in JSON is represented as an array of objects, each containing a set of key-value pairs.
---

**Contents**

[TOC]

### Section 1: List Object
A list object is a JSON structure that contains an ordered list of values. It can be used to represent a collection of objects, such as an array or a list of dictionaries.

### Section 2: Syntax
The syntax for a list object is as follows:
```
[
    <value>,
    <value>,
    ...
]
```

### Section 3: Example
For example, the following JSON structure represents a list of three strings:
```
[
    "apple",
    "banana",
    "orange"
]
```

### Section 4: Nesting
List objects can also be nested, meaning that a list can contain another list as an element. For example, the following JSON structure represents a list of two lists, each containing three strings:
```
[
    [
        "apple",
        "banana",
        "orange"
    ],
    [
        "dog",
        "cat",
        "bird"
    ]
]
```
