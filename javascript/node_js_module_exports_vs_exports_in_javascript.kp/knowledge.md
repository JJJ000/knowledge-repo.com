---
title: What is the difference between module.exports and exports in node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Module.exports is used to export a complete object, while exports is used to export individual properties and methods.
---

**Contents**

[TOC]

### module.exports

`module.exports` is used to define an object that is exported from the module. It is the primary way to expose a module's functionality in Node.js. It can be used to export a single object, a function, or an array of objects and functions.

### exports

`exports` is a shortcut to `module.exports`. It is used to export functions, objects, and primitives from the module. It is important to note that `exports` is not a global object, but rather a reference to `module.exports`. Therefore, any changes made to `exports` will also be made to `module.exports`.
