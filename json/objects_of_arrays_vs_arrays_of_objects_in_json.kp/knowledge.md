---
title: Collection of objects vs single object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: An array of objects is a collection of objects stored in an array, while an object of objects is a collection of objects stored in a single object.
---

**Contents**

[TOC]

1. Array of Objects
An array of objects is an array of individual objects, each with its own set of properties. Each object in the array is a separate entity, and can have its own distinct set of values. For example, an array of objects might look like this: 

[
  {
    "name": "John",
    "age": 30
  },
  {
    "name": "Jane",
    "age": 25
  }
]

2. Object of Objects
An object of objects is an object that contains other objects as its properties. Each of the objects within the parent object can have its own set of values. For example, an object of objects might look like this:

{
  "person1": {
    "name": "John",
    "age": 30
  },
  "person2": {
    "name": "Jane",
    "age": 25
  }
}
