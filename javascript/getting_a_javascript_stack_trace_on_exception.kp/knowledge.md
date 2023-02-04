---
title: What steps do I need to take to generate a JavaScript stack trace when I throw an exception?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the Error.stack property to get a stack trace when you throw an exception in JavaScript.
---

**Contents**

[TOC]

### Using the Error Object

The `Error` object can be used to get a stack trace when an exception is thrown. To do this, you can create an instance of the `Error` object and pass it an error message. The stack trace will be included in the `stack` property of the `Error` object.

```js
try {
  throw new Error('Something went wrong');
} catch (err) {
  console.log(err.stack);
}
```

### Using the Console API

The `console.trace()` method can also be used to get a stack trace when an exception is thrown. This method will print the stack trace to the console, so you can view it in the browser's developer tools.

```js
try {
  throw new Error('Something went wrong');
} catch (err) {
  console.trace();
}
```

### Using the Error.captureStackTrace() Method

The `Error.captureStackTrace()` method can be used to capture the current stack trace and store it in the `stack` property of an `Error` object. This method can be used to get a stack trace when an exception is thrown.

```js
try {
  throw new Error('Something went wrong');
} catch (err) {
  Error.captureStackTrace(err);
  console.log(err.stack);
}
```

### Using a Stack Trace Library

There are also libraries available that can be used to get a stack trace when an exception is thrown. These libraries typically provide more detailed stack traces than the methods mentioned above.
