---
title: What is the syntax for displaying the entire contents of an object using node.js's console.log() instead of '[object]'?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use console.dir() instead of console.log() to get the full object.
---

**Contents**

[TOC]

**1. Using console.dir()**

The console.dir() method allows you to print an object in the console. It outputs a tree-like structure of the object, which is more informative than the default console.log() output.

**2. Using console.table()**

The console.table() method allows you to display an object as a table. This can be useful for quickly viewing the values of an object without having to manually iterate over it.

**3. Using JSON.stringify()**

The JSON.stringify() method allows you to convert an object into a string. This can be useful for printing out the object in a more readable format.

**4. Using a Custom Function**

You can also create a custom function to print out the object in a more readable format. This can be useful if you need to print out the object in a specific way.
