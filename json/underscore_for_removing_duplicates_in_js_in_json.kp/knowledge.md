---
title: Eliminating duplicate items with underscore in javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Underscore`s \_.uniq() method can be used to remove duplicate objects from a JSON array.
---

**Contents**

[TOC]

# Section 1 - Overview
Underscore is a JavaScript library that provides a wide range of utility functions for working with objects, arrays, and other data types. It can be used to remove duplicate objects from JSON data structures.

# Section 2 - Using Underscore to Remove Duplicate Objects
Underscore provides a function called `_.uniq` which can be used to remove duplicate objects from a JSON data structure. This function takes an array as an argument and returns an array containing only the unique objects. To use this function, the array must first be sorted.

# Section 3 - Example
For example, consider the following JSON data structure:

```
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 30
  }
]
```

To remove the duplicate object, we can use the `_.uniq` function as follows:

```
var data = [
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 30
  }
];

var uniqueData = _.uniq(data);

// Result:
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 30
  }
]
```

# Section 4 - Conclusion
Underscore provides a useful utility function for removing duplicate objects from JSON data structures. By using the `_.uniq` function, it is possible to quickly and easily remove duplicate objects from a JSON data structure.
