---
title: Comparing Node.js require and es6 import/export
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Node.js require is used to import modules, while ES6 import/export is used to import and export values from/to modules.
---

**Contents**

[TOC]

# Node.js require
Node.js require is a function used to include modules that exist in separate files. It allows you to include modules in your programs. It takes the form of `require(module)` and you can include a local file, node_modules or a node core module.

# ES6 import/export
ES6 import/export is a way to include modules that exist in separate files. It allows you to include modules in your programs. It takes the form of `import {module} from './module'` and you can include a local file, node_modules or a node core module.

# Differences
The main difference between Node.js require and ES6 import/export is that Node.js require is synchronous while ES6 import/export is asynchronous. Node.js require also allows you to assign the required module to a variable while ES6 import/export does not. Lastly, Node.js require allows you to include a module without using the file path while ES6 import/export requires you to use the file path.
