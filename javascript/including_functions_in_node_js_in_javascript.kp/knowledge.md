---
title: How can I access functions from other files in node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: In Node.js, you can use the `require` function to include functions from other files.
---

**Contents**

[TOC]

1. Using `require()`

The `require()` function is used to include modules that exist in separate files. The basic syntax is:

```javascript
var myModule = require('./myModule');
```

The `require()` function will look for a file called `myModule.js` in the same directory as the file in which the `require()` function is used.

2. Using `module.exports`

The `module.exports` object can be used to define what a module exports and makes available for other modules to require. The syntax for defining a module is:

```javascript
module.exports = {
  myFunction: function() {
    // Function code
  }
};
```

The `myFunction` function can then be used in other modules by requiring the module in which it is defined.

3. Using `exports`

The `exports` object can be used in a similar manner to `module.exports`. The difference is that `exports` is a reference to `module.exports` and changes to `exports` will be reflected in `module.exports`. The syntax is:

```javascript
exports.myFunction = function() {
  // Function code
};
```

The `myFunction` function can then be used in other modules by requiring the module in which it is defined.

4. Using `import`

The `import` statement can be used to import functions from other modules. The syntax is:

```javascript
import {myFunction} from './myModule';
```

The `myFunction` function can then be used in the current module.
