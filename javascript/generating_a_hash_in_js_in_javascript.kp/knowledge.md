---
title: Create a hash from a string using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A Hash can be generated from a string in Javascript using the built-in function `Object.fromEntries()`.
---

**Contents**

[TOC]

### Using the Crypto Library

The Crypto library provides a `createHash()` function for creating a hash from a string.

```javascript
const crypto = require('crypto');

const str = 'My string to hash';

const hash = crypto.createHash('sha256').update(str).digest('hex');

console.log(hash); // Outputs the hash of the string
```

### Using the Node.js Built-in Library

Node.js provides a built-in library for generating hashes from strings.

```javascript
const { createHash } = require('crypto');

const str = 'My string to hash';

const hash = createHash('sha256').update(str).digest('hex');

console.log(hash); // Outputs the hash of the string
```

### Using the Crypto-js Library

The Crypto-js library provides a `SHA256()` function for creating a hash from a string.

```javascript
const CryptoJS = require('crypto-js');

const str = 'My string to hash';

const hash = CryptoJS.SHA256(str).toString();

console.log(hash); // Outputs the hash of the string
```

### Using the Hash.js Library

The Hash.js library provides a `sha256()` function for creating a hash from a string.

```javascript
const hash = require('hash.js');

const str = 'My string to hash';

const hash = hash.sha256().update(str).digest('hex');

console.log(hash); // Outputs the hash of the string
```
