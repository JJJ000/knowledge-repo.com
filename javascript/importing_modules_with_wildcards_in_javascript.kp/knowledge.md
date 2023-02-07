---
title: Can a wildcard be used to import modules from every file in a directory?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, it is not possible to import modules from all files in a directory using a wildcard in Javascript.
---

**Contents**

[TOC]

## No
It is not possible to import modules from all files in a directory using a wildcard in Javascript. 

## Reasons
The reason for this is that Javascript does not support wildcard imports. Wildcard imports are a feature of the ES6 (ECMAScript 2015) specification, which is not yet supported by most browsers. 

## Alternatives
As an alternative, you can use a module bundler, such as Webpack, to bundle all the files in a directory into a single file, which can then be imported. 

## Conclusion
In conclusion, it is not possible to import modules from all files in a directory using a wildcard in Javascript, but there are alternatives available.
