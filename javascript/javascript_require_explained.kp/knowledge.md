---
title: What does the JavaScript "require" command do?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: In JavaScript, `require` is used to import other modules or files into the current script.
---

**Contents**

[TOC]

### Definition

In JavaScript, `require` is a function used to import modules. It is used to load code from external files and use it in the current file. It is a part of the CommonJS module system, which is natively supported in Node.js. 

### Syntax

The syntax for the `require` function is as follows:

```javascript
const module = require('./module');
```

The first argument is the path to the module being imported. This can be a relative path or an absolute path.

### Usage

The `require` function can be used to import code from other JavaScript files. This can be used to separate code into different files, making it easier to maintain.

For example, if you have a file called `math.js` that contains some math functions, you can import them into another file using `require`:

```javascript
// main.js
const math = require('./math');

console.log(math.add(1, 2)); // 3
```

### Alternatives

The `require` function is not the only way to import modules in JavaScript. ES6 also introduced the `import` keyword, which can be used to import modules in a more declarative way. For example:

```javascript
// main.js
import { add } from './math';

console.log(add(1, 2)); // 3
```
