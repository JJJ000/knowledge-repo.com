---
title: What is the process for printing a stack trace in node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To print a stack trace in Node.js, use the `console.trace()` function.
---

**Contents**

[TOC]

#1. Using Error.stack

The Error.stack property of an Error object in Node.js contains the stack trace for that error. This can be accessed and printed directly using the following code:

```
try {
  // Code that could throw an error
} catch (err) {
  console.log(err.stack);
}
```

#2. Using console.trace

The console.trace() method in Node.js prints a stack trace to the console. This can be used to print a stack trace without needing to explicitly catch an error. The following code prints a stack trace to the console:

```
console.trace();
```

#3. Using the V8 Stack Trace API

Node.js provides access to the V8 Stack Trace API, which can be used to programmatically access and print stack traces. The following code prints a stack trace to the console:

```
const { StackTrace } = require('v8');

StackTrace.get().then(stack => console.log(stack));
```

#4. Using the Error.captureStackTrace Method

The Error.captureStackTrace() method in Node.js can be used to capture and print a stack trace for a custom error. The following code prints a stack trace to the console:

```
const { captureStackTrace } = Error;

function CustomError(message) {
  this.message = message;
  captureStackTrace(this, CustomError);
}

try {
  throw new CustomError('Custom Error');
} catch (err) {
  console.log(err.stack);
}
```
