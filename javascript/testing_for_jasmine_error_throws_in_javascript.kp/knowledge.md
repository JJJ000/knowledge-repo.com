---
title: What is the syntax for writing a jasmine test which anticipates an 'error' to be thrown?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `expect(<function>).toThrowError()` matcher to test that an `Error` is thrown in Jasmine.
---

**Contents**

[TOC]

### Section 1: Prepare the Test

The first step in writing a test which expects an 'Error' to be thrown in Jasmine is to prepare the test. This includes defining the function that is expected to throw the error and setting up the Jasmine test.

### Section 2: Create the Expectation

The next step is to create the expectation that the error will be thrown. This is done by using the Jasmine `expect` function, which takes an assertion as its first argument. In this case, the assertion should be `expect(function).toThrowError()`.

### Section 3: Provide the Error

The third step is to provide the error that is expected to be thrown. This can be done by passing an error object as the second argument to the `expect` function.

### Section 4: Run the Test

The final step is to run the test. This can be done by calling the Jasmine `it` function and passing the name of the test as the first argument. The second argument should be a function containing the test code. When the test is run, Jasmine will check to see if the expected error was thrown. If it was, the test will pass; if not, it will fail.
