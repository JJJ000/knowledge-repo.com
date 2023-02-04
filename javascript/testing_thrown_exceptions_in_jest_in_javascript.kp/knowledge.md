---
title: What is the best way to determine the type of an exception thrown in jest?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `toThrow` matcher to test the type of a thrown exception in Jest.
---

**Contents**

[TOC]

### Setting up the Test

Jest provides an easy way to test the type of a thrown exception. First, we need to set up the test.

```javascript
const { throwError } = require('./throwError');

describe('throwError', () => {
  it('should throw an error', () => {
    expect(throwError).toThrow();
  });
});
```

This test will check if the `throwError` function throws an error.

### Testing the Type of the Error

To test the type of the error, we can use the `toThrow` method and pass the type of the error as an argument.

```javascript
const { throwError } = require('./throwError');

describe('throwError', () => {
  it('should throw an error', () => {
    expect(throwError).toThrow(Error);
  });
});
```

This test will check if the `throwError` function throws an `Error`.

### Testing the Error Message

We can also test the error message of the thrown error. To do this, we can use the `toThrow` method and pass the message as an argument.

```javascript
const { throwError } = require('./throwError');

describe('throwError', () => {
  it('should throw an error', () => {
    expect(throwError).toThrow('This is an error');
  });
});
```

This test will check if the `throwError` function throws an error with the message `This is an error`.
