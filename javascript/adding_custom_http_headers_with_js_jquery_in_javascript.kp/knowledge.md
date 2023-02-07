---
title: What is the best way to include a custom http header in an ajax request using JavaScript or jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can add a custom HTTP header to an ajax request with jQuery by using the `beforeSend` callback function.
---

**Contents**

[TOC]

### Using jQuery

jQuery provides an easy way to add custom headers to an AJAX request. The `$.ajax` method takes an argument called `headers` which is an object containing the header names and their corresponding values.

```js
$.ajax({
  url: 'http://example.com/api',
  headers: {
    'X-My-Header': 'MyValue'
  }
});
```

### Using Plain Javascript

In plain Javascript, you can use the `XMLHttpRequest` object to add custom headers. The `setRequestHeader` method is used to set the header name and value.

```js
var xhr = new XMLHttpRequest();
xhr.open('GET', 'http://example.com/api', true);
xhr.setRequestHeader('X-My-Header', 'MyValue');
xhr.send();
```
