---
title: The private key for the Node.js - firebase service account cannot be processed
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The Firebase Service Account Private Key must be decoded from its base64 string format before it can be parsed as JSON.
---

**Contents**

[TOC]

## Parsing Error

When attempting to parse a Firebase Service Account Private Key into JSON, an error may occur. This is due to the fact that the key is encoded in a format called PEM, which is not a valid JSON format.

## Solution

The solution to this issue is to first decode the PEM encoded key into a valid JSON format. This can be done using a library such as the Node.js crypto module. Once the key is decoded, it can then be parsed into a valid JSON object.

## Example

Below is an example of how to decode a Firebase Service Account Private Key and parse it into a valid JSON object:

```
const crypto = require('crypto');

// Decode the PEM encoded key
const decodedKey = crypto.privateDecrypt(
  {
    key: Buffer.from(process.env.FIREBASE_PRIVATE_KEY, 'base64'),
    passphrase: process.env.FIREBASE_PRIVATE_KEY_PASS
  },
  Buffer.from(process.env.FIREBASE_PRIVATE_KEY, 'base64')
);

// Parse the decoded key into a valid JSON object
const parsedKey = JSON.parse(decodedKey);
```
