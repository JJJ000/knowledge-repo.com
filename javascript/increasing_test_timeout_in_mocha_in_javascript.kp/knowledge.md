---
title: What is the procedure for extending the timeout period for an individual test case in mocha?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can increase the timeout for a single test case in Mocha by using the `this.timeout` function within the test case.
---

**Contents**

[TOC]

## Setting Timeout Globally

Mocha allows users to adjust the timeout globally for all test cases. This can be done by setting the `--timeout` flag when running the tests. For example, if you wanted to set the timeout to 2000 milliseconds, you could run the command `mocha --timeout 2000`.

## Setting Timeout Per Test Case

Mocha also allows users to set the timeout for individual test cases. This can be done by using the `this.timeout()` method inside of the test case. For example, if you wanted to set the timeout to 1000 milliseconds for a single test case, you could do the following:

```javascript
it('should do something', function() {
  this.timeout(1000);
  // test code
});
```

## Overriding Global Timeout

The timeout set for individual test cases will override the global timeout set with the `--timeout` flag. This can be useful if you want to set a longer timeout for certain tests that require more time.

## Setting Default Timeout

Mocha also allows users to set a default timeout for all test cases. This can be done by setting the `DEFAULT_TIMEOUT_INTERVAL` variable in the `mocha.opts` file. For example, if you wanted to set the default timeout to 3000 milliseconds, you could add the following line to the `mocha.opts` file:

`--timeout 3000`
