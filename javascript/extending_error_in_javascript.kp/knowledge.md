---
title: How can I expand upon the error class in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Create a custom Error class by extending the built-in Error class and adding custom properties and methods.
---

**Contents**

[TOC]

#### Creating a Custom Error
Creating a custom error in JavaScript is fairly simple. First, create a new class that extends the Error class. The constructor for the class should take two parameters: a message string and an optional error code.

```js
class CustomError extends Error {
  constructor(message, code) {
    super(message);
    this.name = this.constructor.name;
    this.code = code;
  }
}
```

#### Adding Custom Properties
In addition to the standard properties of the Error class, you can add custom properties to your custom error class. This allows you to provide additional context for the error.

```js
class CustomError extends Error {
  constructor(message, code) {
    super(message);
    this.name = this.constructor.name;
    this.code = code;
    this.additionalInfo = {};
  }
}
```

#### Throwing the Error
When you need to throw the error, simply create a new instance of your custom error class and throw it.

```js
try {
  // Code that may throw an error
} catch (err) {
  throw new CustomError('Something went wrong', err.code);
}
```

#### Handling the Error
When handling the error, you can access the custom properties you added to the error.

```js
try {
  // Code that may throw an error
} catch (err) {
  if (err instanceof CustomError) {
    // Do something with err.additionalInfo
  }
}
```
