---
title: Do you have the ability to create asynchronous tests that anticipate an exception being thrown?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, it is possible to write async tests that expect toThrow in Javascript using the `.catch()` method.
---

**Contents**

[TOC]

## Setup

In order to write an asynchronous test that expects toThrow in Javascript, we will need to set up our environment. This includes importing the necessary libraries, such as `jest` and `expect`, as well as any other libraries or modules needed for the test.

## Writing the Test

Once we have our environment set up, we can write the test itself. The test should include an asynchronous `expect` statement that uses the `toThrow` method. This method will be used to check that the expected error is thrown. For example:

```javascript
expect(async () => {
  // code that should throw an error
}).toThrow();
```

## Running the Test

Finally, we can run the test using the `jest` command. This will execute the asynchronous test and check that the expected error is thrown.

## Verifying the Results

Once the test has been run, we can verify the results. We can check the output of the test to make sure that the expected error was thrown, and that no other errors were encountered.
