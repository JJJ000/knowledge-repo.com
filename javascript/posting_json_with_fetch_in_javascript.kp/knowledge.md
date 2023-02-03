---
title: Retrieve submit JSON information
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To POST JSON data in Javascript, use the XMLHttpRequest.send() method.
---

**Contents**

[TOC]

#### Sending JSON Data

To send JSON data in a POST request, the `Content-Type` header must be set to `application/json`. The body of the request should contain the JSON string.

In JavaScript, this can be done using the `XMLHttpRequest` object:

```javascript
var xhr = new XMLHttpRequest();
xhr.open("POST", "https://example.com/data", true);
xhr.setRequestHeader('Content-Type', 'application/json');
xhr.send(JSON.stringify({data: 'value'}));
```

#### Processing the Response

Once the request is sent, the response can be processed using the `onload` event handler. The response can be accessed using the `responseText` property of the `XMLHttpRequest` object. This will contain the response body in string format, which can then be parsed as JSON:

```javascript
xhr.onload = function () {
  if (xhr.status >= 200 && xhr.status < 300) {
    var response = JSON.parse(xhr.responseText);
    // Do something with the response
  }
};
```

#### Error Handling

It is important to handle any errors that may occur during the request. This can be done using the `onerror` event handler:

```javascript
xhr.onerror = function () {
  // Handle the error
};
```
