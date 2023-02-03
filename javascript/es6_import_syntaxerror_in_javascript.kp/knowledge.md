---
title: The import statement cannot be used outside of an ecmascript 6 module, which has caused an uncaught syntaxerror
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: This error occurs because ES6 imports are only supported in modules, not in scripts.
---

**Contents**

[TOC]

# Solution

## Overview
This error occurs when attempting to use the ES6 import statement outside of a module. The import statement is only available within modules, which are a feature of ES6.

## Explanation
The import statement is used to import functions, objects, and primitives from other modules. It is only available within modules, which are a feature of ES6. When attempting to use the import statement outside of a module, the browser will throw an error.

## Workaround
If you are not using a module, you can use the require() method instead. The require() method is available in both ES5 and ES6 and can be used to import functions, objects, and primitives from other files.

## Conclusion
Using the import statement outside of a module will result in an error. To avoid this error, you should use the require() method instead.
