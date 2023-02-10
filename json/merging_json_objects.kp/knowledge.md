---
title: Combine two JSON objects
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can concatenate two JSON objects by combining their properties and values into a single object.
---

**Contents**

[TOC]

## Section 1: Definition

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays.

## Section 2: Concatenation

Concatenation is the process of combining two or more JSON objects into a single object. This can be accomplished by using the `Object.assign()` method, which takes two or more objects as arguments and returns a new object with the properties of all the objects combined.

## Section 3: Example

Let's say we have two JSON objects:

```
let obj1 = {
  name: "John",
  age: 30
};

let obj2 = {
  city: "New York",
  state: "NY"
};
```

We can combine these two objects using the `Object.assign()` method:

```
let obj3 = Object.assign(obj1, obj2);
```

The resulting object `obj3` would be:

```
{
  name: "John",
  age: 30,
  city: "New York",
  state: "NY"
}
```

## Section 4: Conclusion

Concatenating two JSON objects is a simple process that can be accomplished using the `Object.assign()` method. This method takes two or more objects as arguments and returns a new object with the properties of all the objects combined.
