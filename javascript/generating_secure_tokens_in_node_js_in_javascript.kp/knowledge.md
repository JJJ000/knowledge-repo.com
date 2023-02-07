---
title: Generating a secure, random token using node.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: A cryptographically secure random token can be generated in Node.js using the crypto module`s randomBytes() function.
---

**Contents**

[TOC]

### Using the Crypto Library

The `crypto` library in Node.js can be used to generate cryptographically secure random tokens.

To generate a random token, the `crypto.randomBytes()` function can be used. This function accepts a number of bytes as an argument and returns a `Buffer` object with random bytes.

```javascript
const crypto = require('crypto');

const token = crypto.randomBytes(32).toString('hex');
```

The `token` variable now holds a 32-byte random hexadecimal string.

### Using the UUID Library

The `uuid` library in Node.js can also be used to generate random tokens. This library provides a function `v4()` which returns a random UUID string.

```javascript
const uuid = require('uuid');

const token = uuid.v4();
```

The `token` variable now holds a random UUID string.
