---
title: The difference between "module.exports" and "exports" in the commonjs module system is that "module.exports" is an object that is exposed as the module interface, while "exports" is a reference to "module.exports" that allows developers to add properties to the exported object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: `module.exports` is used to export an entire module, while `exports` is used to export specific parts of a module.
---

**Contents**

[TOC]

### Definition

`module.exports` is an object that is used to export objects, functions, strings, or any other type of data from a JavaScript file. `exports` is an object that is used to export objects, functions, strings, or any other type of data from a JavaScript file.

### Differences

1. `module.exports` is used to export a single object or constructor function while `exports` is used to export multiple objects or functions.

2. `module.exports` is used to export an object by reference while `exports` is used to export an object by value.

3. `module.exports` is used to export the module for use in other modules while `exports` is used to export the module for use in the current file.
