---
title: Retrieve the values from the "get" variables (javascript)
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the built-in `URLSearchParams` object to get the values from the GET parameters.
---

**Contents**

[TOC]

### Using the `URL` Object

The `URL` object can be used to parse the query string from the current page's URL.

```js
// Get the current page's URL
const pageURL = window.location.href;

// Create a new URL object
const url = new URL(pageURL);

// Parse the query string
const queryParams = url.searchParams;

// Get the value of the "GET" parameter
const getParamValue = queryParams.get('paramName');
```

### Using the `URLSearchParams` Object

The `URLSearchParams` object can be used to parse the query string from the current page's URL.

```js
// Get the current page's URL
const pageURL = window.location.href;

// Create a new URLSearchParams object
const queryParams = new URLSearchParams(pageURL);

// Get the value of the "GET" parameter
const getParamValue = queryParams.get('paramName');
```

### Using the `URL` and `URLSearchParams` Objects

The `URL` and `URLSearchParams` objects can be used together to parse the query string from the current page's URL.

```js
// Get the current page's URL
const pageURL = window.location.href;

// Create a new URL object
const url = new URL(pageURL);

// Create a new URLSearchParams object
const queryParams = new URLSearchParams(url.search);

// Get the value of the "GET" parameter
const getParamValue = queryParams.get('paramName');
```

### Using the `location.search` Property

The `location.search` property can be used to parse the query string from the current page's URL.

```js
// Get the query string from the current page's URL
const queryString = window.location.search;

// Create a new URLSearchParams object
const queryParams = new URLSearchParams(queryString);

// Get the value of the "GET" parameter
const getParamValue = queryParams.get('paramName');
```
