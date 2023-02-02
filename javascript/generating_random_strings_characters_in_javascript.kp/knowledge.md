---
title: Create a random string/characters in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Math.random().toString(36).substring(2, 15) can be used to generate a random string of characters in JavaScript.
---

**Contents**

[TOC]

# Option 1: Using Math.random

This is the simplest and most straightforward way of generating random strings or characters.

```javascript
function generateRandomString(length) {
  let result = '';
  let characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
  let charactersLength = characters.length;
  for (let i = 0; i < length; i++) {
    result += characters.charAt(Math.floor(Math.random() * charactersLength));
  }
  return result;
}

// Usage
let randomString = generateRandomString(10); // output: "6jfYh2G1mK"
```

# Option 2: Using Cryptographically Secure Library

This option requires the use of a cryptographically secure library. For example, the `crypto` module in Node.js.

```javascript
const crypto = require('crypto');

function generateRandomString(length) {
  return crypto.randomBytes(Math.ceil(length / 2))
    .toString('hex')
    .slice(0, length);
};

// Usage
let randomString = generateRandomString(10); // output: "fdbmmz79n9"
```

# Option 3: Using uuid

This option requires the use of the `uuid` package.

```javascript
const uuidv4 = require('uuid/v4');

function generateRandomString(length) {
  let result = uuidv4();
  return result.substring(0, length);
};

// Usage
let randomString = generateRandomString(10); // output: "7f6d2f8aec"
```

# Option 4: Using Chance

This option requires the use of the `chance` package.

```javascript
const Chance = require('chance');

function generateRandomString(length) {
  let chance = new Chance();
  return chance.string({length: length});
};

// Usage
let randomString = generateRandomString(10); // output: "6d2f8aec7f"
```
