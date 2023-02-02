---
title: Convert a url to a string of encoded characters using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the encodeURIComponent() function to encode a URL in JavaScript.
---

**Contents**

[TOC]

1. **Using encodeURI() Method**

The JavaScript `encodeURI()` method is used to encode a URI by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character. For example, the character "#" is replaced by the string "%23".

```
var uri = "https://www.example.com/test?name=John#foo";
var encodedUri = encodeURI(uri);
console.log(encodedUri); // "https://www.example.com/test?name=John%23foo"
```

2. **Using encodeURIComponent() Method**

The JavaScript `encodeURIComponent()` method is used to encode a URI component by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character. For example, the character "#" is replaced by the string "%23".

```
var uriComponent = "https://www.example.com/test?name=John#foo";
var encodedUriComponent = encodeURIComponent(uriComponent);
console.log(encodedUriComponent); // "https%3A%2F%2Fwww.example.com%2Ftest%3Fname%3DJohn%23foo"
```

3. **Using escape() Method**

The JavaScript `escape()` method is used to encode a string by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character. For example, the character "#" is replaced by the string "%23".

```
var str = "https://www.example.com/test?name=John#foo";
var encodedStr = escape(str);
console.log(encodedStr); // "https%3A//www.example.com/test%3Fname%3DJohn%23foo"
```

4. **Using encode() Method**

The JavaScript `encode()` method is used to encode a string by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character. For example, the character "#" is replaced by the string "%23".

```
var str = "https://www.example.com/test?name=John#foo";
var encodedStr = encode(str);
console.log(encodedStr); // "https%3A//www.example.com/test%3Fname%3DJohn%23foo"
```
