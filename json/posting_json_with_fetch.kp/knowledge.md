---
title: Retrieve: How to send JSON data via POST?
authors:
- cool_wizard
tags:
- api
- javascript
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-22 00:00:00
updated_at: 2023-01-22 00:00:00
tldr: You can use the fetch API to make a POST request and receive a JSON response.
---

**Contents**

[TOC]

### Setting Headers

To send JSON data with a POST request, you need to set the `Content-Type` header to `application/json`. This lets the server know that the body content is in JSON format.

### Stringifying Data

The data needs to be stringified before it is sent. This means that it must be converted from a JavaScript object into a string format. You can do this using the `JSON.stringify()` method.

### Sending the Request

Once the data is stringified, you can send the request using the `fetch()` API. The `fetch()` API takes two arguments: the URL of the request and an options object. The options object should contain the method (POST) and the body (the stringified JSON data).

### Handling the Response

When the response is received, it needs to be parsed back into a JavaScript object. This can be done using the `JSON.parse()` method. Once the response is parsed, you can use it in your application.
