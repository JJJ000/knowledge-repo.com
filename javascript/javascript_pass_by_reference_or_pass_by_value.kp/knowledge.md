---
title: What kind of parameter passing does JavaScript use pass-by-reference or pass-by-value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: JavaScript is a pass-by-value language.
---

**Contents**

[TOC]

# Pass-by-Value
In JavaScript, primitive values (strings, numbers, booleans, etc.) are always passed by value. When a primitive value is passed to a function, a copy of the value is created and passed to the function. The original value is not affected by any changes made to the copy.

# Pass-by-Reference
In JavaScript, objects are passed by reference. When an object is passed to a function, the function will get a reference to the object, not a copy of the object. Changes made to the object within the function will be reflected in the original object.
