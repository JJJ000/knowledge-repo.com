---
title: What are the steps to configure headers and options in axios?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To set headers and options in axios, use the axios.defaults.headers.common and axios.defaults.options properties.
---

**Contents**

[TOC]

## Setting Header

Axios provides a `headers` configuration option to set headers. This option can be set as an object, an array of objects, or a function returning an object or an array of objects.

```javascript
axios.get('/user', {
  headers: {
    'X-Requested-With': 'XMLHttpRequest',
    'Authorization': 'Bearer <token>'
  }
});
```

## Setting Options

Axios provides a `options` configuration option for setting options. This option can be set as an object, an array of objects, or a function returning an object or an array of objects.

```javascript
axios.get('/user', {
  options: {
    timeout: 5000,
    maxRedirects: 5
  }
});
```
