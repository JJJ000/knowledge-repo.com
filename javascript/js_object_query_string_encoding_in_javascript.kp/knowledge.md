---
title: Encoding a JavaScript object into a query string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The query-string encoding of a JavaScript object can be achieved by using the built-in JavaScript function `encodeURIComponent()`.
---

**Contents**

[TOC]

### 1. Create Query String

```javascript
let obj = {
  name: "John",
  age: 25
};

let queryString = Object.keys(obj).map(key => key + '=' + obj[key]).join('&');

console.log(queryString); // name=John&age=25
```

### 2. Encode Query String

```javascript
let encodedQueryString = encodeURIComponent(queryString);

console.log(encodedQueryString); // name%3DJohn%26age%3D25
```

### 3. Decode Query String

```javascript
let decodedQueryString = decodeURIComponent(encodedQueryString);

console.log(decodedQueryString); // name=John&age=25
```

### 4. Parse Query String

```javascript
let parsedQueryString = decodedQueryString.split('&').reduce((acc, curr) => {
  let parts = curr.split('=');
  acc[parts[0]] = parts[1];
  return acc;
}, {});

console.log(parsedQueryString); // {name: "John", age: "25"}
```
