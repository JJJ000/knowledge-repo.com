---
title: The json.stringify method cannot be used to convert a normal JavaScript array into a string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: No, JSON.stringify does not work with normal Javascript arrays.
---

**Contents**

[TOC]

### No

JSON.stringify() is used to convert a JavaScript object into a string. It does not work with normal JavaScript arrays, as these are not objects.

### What JSON.stringify() Does

JSON.stringify() takes a JavaScript object and converts it into a string. The resulting string is a valid JSON format, which can be parsed by any valid JSON parser.

### What JSON.stringify() Does Not Do

JSON.stringify() does not work with normal JavaScript arrays, as these are not objects. This means that if you try to use JSON.stringify() on an array, it will not work.

### Alternatives

If you want to convert an array into a JSON string, you can use the JSON.stringify() method on each element of the array, and then join them together into a single string.
