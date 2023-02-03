---
title: How can I make jquery perform an ajax request that is synchronous, instead of asynchronous?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use the `async false` option in the jQuery Ajax request.
---

**Contents**

[TOC]

### Synchronous vs. Asynchronous Requests

Ajax requests are typically asynchronous, meaning that the request is sent to the server and the code continues to execute without waiting for a response. This is useful for keeping webpages responsive and allowing multiple requests to be made at the same time.

Synchronous requests, on the other hand, wait for the server to respond before continuing execution. This can be useful when the response from the server is needed before the rest of the code can be executed.

### jQuery

jQuery is a popular JavaScript library for making Ajax requests. By default, jQuery sends asynchronous requests.

### Making a Synchronous Request

To make a synchronous request with jQuery, the `async` option must be set to `false` when making the request:

```javascript
$.ajax({
    url: 'example.com',
    type: 'GET',
    async: false
});
```

By setting `async` to `false`, the request will be sent synchronously and the code will wait for the response before continuing execution.
