---
title: What is the function of Node.js module.exports and how do you implement it?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Node.js module.exports is used to export functions, objects, or values from a Node.js file, so they can be imported and used in other files.
---

**Contents**

[TOC]

## What is module.exports?

module.exports is a special object in Node.js used to expose variables and functions to other modules. It is the primary way to share code between files, and is used to create Node.js modules.

## How is it used?

When writing a module in Node.js, the module code is wrapped in a function with the module name as an argument. Inside the function, the module.exports object can be used to add properties and methods that can be accessed by other modules.

For example, if a module is named "math", the following code can be used to add a function named "add" to the module.exports object:

```js
module.exports.add = function(a, b) {
  return a + b;
};
```

## How is it accessed?

To access the module from another file, the require() function is used. The require() function takes a single argument, which is the name of the module. For example, if the module is named "math", the following code can be used to access the add function from the module:

```js
const math = require('math');
const result = math.add(2, 3);
```

## Conclusion

module.exports is a powerful tool in Node.js that allows modules to be shared and reused between files. It is used to add properties and methods to the module.exports object, and can be accessed using the require() function.
