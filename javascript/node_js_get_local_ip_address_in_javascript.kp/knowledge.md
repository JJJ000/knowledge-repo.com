---
title: Find the local ip address in node.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The local IP address can be retrieved using the `require(`os`).networkInterfaces()` method.
---

**Contents**

[TOC]

### Using the Node.js `os` Module

The easiest way to get the local IP address of a machine in Node.js is to use the `os` module. The `os` module provides a few methods to get the local IP address of the machine.

### Example

The following example uses the `os.networkInterfaces()` method to get the local IP address of the machine.

```javascript
const os = require('os');

const interfaces = os.networkInterfaces();
let ipAddress;

Object.keys(interfaces).forEach(function (interface) {
  interfaces[interface].forEach(function (address) {
    if (address.family === 'IPv4' && !address.internal) {
      ipAddress = address.address;
    }
  });
});

console.log(ipAddress);
```

### Using the Node.js `dns` Module

Another way to get the local IP address of a machine in Node.js is to use the `dns` module. The `dns` module provides a few methods to get the local IP address of the machine.

### Example

The following example uses the `dns.lookup()` method to get the local IP address of the machine.

```javascript
const dns = require('dns');

dns.lookup(os.hostname(), function (err, address) {
  console.log(address);
});
```
