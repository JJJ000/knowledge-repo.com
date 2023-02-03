---
title: What is the process for converting a string to base64 in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can encode a string to Base64 in JavaScript using the btoa() function.
---

**Contents**

[TOC]

## Encoding a String to Base64

1. Create a string to be encoded.

```javascript
let stringToEncode = "Hello World!";
```

2. Use the `btoa()` function to encode the string.

```javascript
let encodedString = btoa(stringToEncode);
```

3. The encoded string is now ready to be used.

```javascript
console.log(encodedString); // Outputs "SGVsbG8gV29ybGQh"
```

## Decoding a Base64 String

1. Create a string to be decoded.

```javascript
let stringToDecode = "SGVsbG8gV29ybGQh";
```

2. Use the `atob()` function to decode the string.

```javascript
let decodedString = atob(stringToDecode);
```

3. The decoded string is now ready to be used.

```javascript
console.log(decodedString); // Outputs "Hello World!"
```
