---
title: What is the best way to access query string values in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the `URLSearchParams` object to get query string values in JavaScript.
---

**Contents**

[TOC]

## Using URLSearchParams

The URLSearchParams interface provides a consistent interface for retrieving the query string parameters from the URL.

```js
const urlParams = new URLSearchParams(window.location.search);
const myParam = urlParams.get('myParam');
```

## Using the Location Object

The `location` object contains information about the current URL. This object can be used to get query string parameters from the URL.

```js
const queryString = window.location.search;
const urlParams = new URLSearchParams(queryString);
const myParam = urlParams.get('myParam');
```

## Using Regular Expressions

Regular expressions can be used to extract query string parameters from the URL.

```js
const queryString = window.location.search;
const myParam = queryString.match(/myParam=([^&]*)/)[1];
```

## Using a Library

There are several libraries available that provide utility functions for extracting query string parameters from the URL.

For example, the `qs` library can be used to extract query string parameters from the URL.

```js
const qs = require('qs');
const queryString = window.location.search;
const params = qs.parse(queryString);
const myParam = params.myParam;
```
