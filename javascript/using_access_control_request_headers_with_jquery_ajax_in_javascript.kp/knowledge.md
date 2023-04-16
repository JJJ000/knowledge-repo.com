---
title: Jquery can be used to add the 'access control request headers' to the header of an ajax request
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, the Access Control Request Headers can be added to the header of an AJAX request with jQuery in Javascript.
---

**Contents**

[TOC]

# Yes

When making an AJAX request with jQuery in Javascript, the `Access-Control-Request-Headers` header can be included in the request.

# How

This can be done by adding the `Access-Control-Request-Headers` header to the `headers` option of the jQuery `$.ajax()` method. For example:

```javascript
$.ajax({
    url: 'http://example.com/api',
    type: 'POST',
    headers: {
        'Access-Control-Request-Headers': 'x-requested-with'
    },
    success: function (data) {
        // Do something with the response data
    }
});
```

# Why

This header is used to indicate which headers are allowed to be sent in a cross-origin request. This helps to prevent malicious requests from being sent to a server.
