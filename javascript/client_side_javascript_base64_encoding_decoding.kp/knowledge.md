---
title: Encoding and decoding base64 in JavaScript on the client side
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Base64 encoding and decoding can be done in client-side Javascript using the btoa() and atob() functions.
---

**Contents**

[TOC]

### Base64 Encoding

Base64 encoding is a way to encode binary data (such as an image) into ASCII characters. In client-side Javascript, the `btoa()` function can be used to convert a string to Base64.

For example:

```javascript
var encodedString = btoa('Hello World!');
// encodedString = "SGVsbG8gV29ybGQh"
```

### Base64 Decoding

Base64 decoding is the process of converting a Base64 encoded string back into its original binary form. In client-side Javascript, the `atob()` function can be used to convert a Base64 encoded string to its original form.

For example:

```javascript
var decodedString = atob('SGVsbG8gV29ybGQh');
// decodedString = "Hello World!"
```

### Browser Support

The `btoa()` and `atob()` functions are supported in most modern browsers, including Chrome, Firefox, Safari, and Edge. It is also supported in Internet Explorer 10 and later.
