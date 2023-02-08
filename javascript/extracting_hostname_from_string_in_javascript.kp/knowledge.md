---
title: Get the hostname from the string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The hostname can be extracted from a string using the JavaScript string method `split()` with the delimiter `//`.
---

**Contents**

[TOC]

### Using Regular Expressions

The following regular expression can be used to extract the hostname from a string:

`/^(?:https?:\/\/)?(?:[^@\n]+@)?(?:www\.)?([^:\/\n]+)/im`

To use this regular expression, you can use the `String.prototype.match()` method, as shown in the following example:

```javascript
let str = 'https://www.example.com';
let hostname = str.match(/^(?:https?:\/\/)?(?:[^@\n]+@)?(?:www\.)?([^:\/\n]+)/im)[1];
// Output: 'example.com'
```

### Using the URL API

The URL API provides a convenient way to extract the hostname from a string. The `URL` constructor can be used to create a URL object from a string, and the `hostname` property can be used to get the hostname of the URL.

For example:

```javascript
let str = 'https://www.example.com';
let url = new URL(str);
let hostname = url.hostname;
// Output: 'example.com'
```

### Using the Node.js URL Module

If you are using Node.js, you can also use the `url` module to extract the hostname from a string. The `url.parse()` method can be used to parse a URL string into a URL object, and the `hostname` property can be used to get the hostname of the URL.

For example:

```javascript
const url = require('url');

let str = 'https://www.example.com';
let urlObject = url.parse(str);
let hostname = urlObject.hostname;
// Output: 'example.com'
```
