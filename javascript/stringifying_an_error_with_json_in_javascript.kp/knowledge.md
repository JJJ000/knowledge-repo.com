---
title: Can you stringify an error using json.stringify?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: No, it is not possible to stringify an Error using JSON.stringify in Javascript.
---

**Contents**

[TOC]

### No

JSON.stringify does not support Error objects. If an Error object is passed to JSON.stringify, it will be treated as an object and converted to a string.

### Why

Error objects contain a stack property which is a non-enumerable property. This means that the property will not be included in the stringification process.

### Alternatives

If you want to stringify an Error object, you can use the Error.prototype.toString() method. This will convert the Error object to a string that can be used for logging or debugging.
