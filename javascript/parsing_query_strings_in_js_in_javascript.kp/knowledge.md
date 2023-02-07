---
title: Analyze the query string using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The query string can be parsed using the built-in JavaScript function `URLSearchParams()`.
---

**Contents**

[TOC]

# 1. Using the `URL` Object

The `URL` object can be used to parse query strings in JavaScript. It provides a number of useful methods to get the query string values.

```javascript
const url = new URL('http://example.com?foo=bar&baz=qux');
const foo = url.searchParams.get('foo'); // "bar"
const baz = url.searchParams.get('baz'); // "qux"
```

# 2. Using the `URLSearchParams` Object

The `URLSearchParams` object can be used to parse query strings in JavaScript. It provides a number of useful methods to get the query string values.

```javascript
const paramsString = 'foo=bar&baz=qux';
const params = new URLSearchParams(paramsString);
const foo = params.get('foo'); // "bar"
const baz = params.get('baz'); // "qux"
```

# 3. Using the `split` and `forEach` Methods

The `split` and `forEach` methods can be used to parse query strings in JavaScript.

```javascript
const paramsString = 'foo=bar&baz=qux';
const params = {};
paramsString.split('&').forEach(param => {
  const [key, value] = param.split('=');
  params[key] = value;
});
const foo = params.foo; // "bar"
const baz = params.baz; // "qux"
```

# 4. Using the `reduce` Method

The `reduce` method can be used to parse query strings in JavaScript.

```javascript
const paramsString = 'foo=bar&baz=qux';
const params = paramsString.split('&').reduce((acc, param) => {
  const [key, value] = param.split('=');
  acc[key] = value;
  return acc;
}, {});
const foo = params.foo; // "bar"
const baz = params.baz; // "qux"
```
