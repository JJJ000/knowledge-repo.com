---
title: Verify if a JavaScript string is a url
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the RegExp method test() to check if a string is a URL.
---

**Contents**

[TOC]

##### Using Regular Expression

We can use a regular expression to check if a string is a URL. The following expression will check for URLs starting with `http://`, `https://`, `ftp://` or `file://`:

```javascript
let urlRegex = /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/;

let str = 'http://www.example.com';

urlRegex.test(str); // returns true
```

##### Using URL Object

We can also use the `URL` object to check if a string is a URL. The `URL` object will throw a `TypeError` if the string is not a valid URL.

```javascript
let str = 'http://www.example.com';

try {
  let url = new URL(str);
  // If the string is a valid URL, the code will reach this line
  console.log('Valid URL');
} catch (e) {
  // If the string is not a valid URL, the code will reach this line
  console.log('Invalid URL');
}
```

##### Using Location Object

We can also use the `Location` object to check if a string is a URL. The `Location` object will throw a `SyntaxError` if the string is not a valid URL.

```javascript
let str = 'http://www.example.com';

try {
  window.location = str;
  // If the string is a valid URL, the code will reach this line
  console.log('Valid URL');
} catch (e) {
  // If the string is not a valid URL, the code will reach this line
  console.log('Invalid URL');
}
```
