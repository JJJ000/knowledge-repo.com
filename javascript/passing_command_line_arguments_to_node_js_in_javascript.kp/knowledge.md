---
title: What is the syntax for passing command line arguments to a Node.js program?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can pass command line arguments to a Node.js program using the process.argv array.
---

**Contents**

[TOC]

# Section 1: Using process.argv

The `process.argv` property returns an array containing the command line arguments passed when the Node.js process was launched. This array will always have at least two elements: the path to the Node.js executable and the path to the JavaScript file being executed. 

# Section 2: Accessing Command Line Arguments

To access the command line arguments, we can use the `slice()` method to create a new array that contains all the arguments starting from the third element of the `process.argv` array. 

```javascript
const args = process.argv.slice(2);
```

# Section 3: Parsing Arguments

Once we have the array of arguments, we can parse them using the `forEach()` method. 

```javascript
args.forEach(arg => {
  // Parse each argument
});
```

# Section 4: Using a Third-Party Library

Alternatively, we can use a third-party library, such as [minimist](https://www.npmjs.com/package/minimist), to parse command line arguments in a more structured way. 

```javascript
const args = require('minimist')(process.argv.slice(2));
```
