---
title: What is the procedure for executing an individual test with mocha?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Run `mocha <test-file-name>` in the terminal to run a single test with Mocha in Javascript.
---

**Contents**

[TOC]

## Step 1: Install Mocha

Mocha is a JavaScript test framework that runs on Node.js and in the browser. To install Mocha, run the following command in your terminal:

```
npm install --global mocha
```

## Step 2: Create a Test File

Create a JavaScript file that contains the test code. For example, create a test file called `mytest.js` with the following content:

```
const assert = require('assert');

describe('my test', () => {
  it('should pass', () => {
    assert.equal(1, 1);
  });
});
```

## Step 3: Run the Test

Run the test using the following command:

```
mocha mytest.js
```

## Step 4: Check the Results

The results of the test will be displayed in the terminal. If the test passes, you should see the following output:

```
my test
    ✓ should pass

1 passing (5ms)
```
