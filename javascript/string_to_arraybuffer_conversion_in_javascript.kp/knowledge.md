---
title: Transforming between strings and arraybuffers
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the built-in functions TextDecoder and TextEncoder to convert between strings and ArrayBuffers.
---

**Contents**

[TOC]

#### String to ArrayBuffer

The `TextEncoder` and `TextDecoder` interfaces provide methods to convert strings to ArrayBuffers and vice versa.

To convert a string to an ArrayBuffer, use the `TextEncoder` interface to encode the string as a UTF-8 encoded `Uint8Array` and then call the `buffer` method on the `Uint8Array` to get the ArrayBuffer.

```js
const encoder = new TextEncoder();
const string = 'Hello world!';
const arrayBuffer = encoder.encode(string).buffer;
```

#### ArrayBuffer to String

To convert an ArrayBuffer to a string, use the `TextDecoder` interface to decode the `Uint8Array` from the ArrayBuffer and then call the `decode` method on the `Uint8Array` to get the string.

```js
const decoder = new TextDecoder();
const arrayBuffer = ...;
const string = decoder.decode(new Uint8Array(arrayBuffer));
```
