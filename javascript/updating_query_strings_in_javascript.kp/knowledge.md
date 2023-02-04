---
title: What is the process for changing or adding a query string parameter?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can add or update a query string parameter in Javascript by using the URLSearchParams API.
---

**Contents**

[TOC]

### Using the URL Interface

The URL interface allows us to manipulate the query string of a given URL. We can use the `searchParams` property of the URL interface to access and modify the query string.

To add a query string parameter, we can use the `append()` method of the `searchParams` property. This method takes two arguments: the name of the parameter and its value.

Example:

```js
const url = new URL('https://example.com');
url.searchParams.append('foo', 'bar');
console.log(url.href); // https://example.com?foo=bar
```

To update an existing query string parameter, we can use the `set()` method of the `searchParams` property. This method also takes two arguments: the name of the parameter and its value.

Example:

```js
const url = new URL('https://example.com?foo=bar');
url.searchParams.set('foo', 'baz');
console.log(url.href); // https://example.com?foo=baz
```

### Using the URLSearchParams Interface

The URLSearchParams interface allows us to manipulate the query string of a given URL. We can use the `append()` and `set()` methods of the URLSearchParams interface to add or update a query string parameter.

To add a query string parameter, we can use the `append()` method. This method takes two arguments: the name of the parameter and its value.

Example:

```js
const params = new URLSearchParams();
params.append('foo', 'bar');
console.log(params.toString()); // foo=bar
```

To update an existing query string parameter, we can use the `set()` method. This method also takes two arguments: the name of the parameter and its value.

Example:

```js
const params = new URLSearchParams('foo=bar');
params.set('foo', 'baz');
console.log(params.toString()); // foo=baz
```
