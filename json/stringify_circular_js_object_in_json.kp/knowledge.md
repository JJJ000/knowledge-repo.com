---
title: Convert a JavaScript object with circular references into a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: It is not possible to stringify a JavaScript object with circular reference in JSON.
---

**Contents**

[TOC]

### Section 1: Circular Reference
A circular reference is a situation in which an object contains a reference to itself. In JavaScript, this can be done by setting a variable to itself, or by creating an object that contains a reference to itself.

### Section 2: Stringify
Stringifying a JavaScript object with a circular reference can be done using the `JSON.stringify()` method. This method takes the object as an argument and returns a string representation of the object.

### Section 3: Limitations
However, this method has some limitations when it comes to dealing with circular references. In particular, it will not be able to stringify an object that contains a reference to itself.

### Section 4: Solution
To stringify an object with a circular reference, you can use a library such as the `circular-json` library. This library provides a `stringify()` method that can be used to stringify objects with circular references.
