---
title: Making a request to a JSON API using node.js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: To call a JSON API with Node.js, you can use the built-in `fetch()` function to make an HTTP request and parse the response as JSON.
---

**Contents**

[TOC]

**Section 1: Setting Up the Request**

To call a JSON API with Node.js, the first step is to set up a request. This can be done using the built-in `http` module. The `http.request()` method takes a URL as an argument and returns an object representing the request. This object can then be used to send the request and receive a response.

**Section 2: Sending the Request**

Once the request is set up, it can be sent using the `.end()` method. This method accepts an optional data argument, which can be used to specify any data that should be sent along with the request. The `.end()` method also takes a callback that will be called when the response is received.

**Section 3: Parsing the Response**

When the response is received, it can be parsed using the `JSON.parse()` method. This method takes a string of JSON data as an argument and returns a JavaScript object. This object can then be used to access the data contained in the response.

**Section 4: Handling Errors**

It is important to handle any errors that may occur when calling a JSON API with Node.js. This can be done by checking the `response.statusCode` property to make sure it is in the 200-299 range. If it is not, an error has occurred and should be handled appropriately.
