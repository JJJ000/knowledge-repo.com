---
title: What is the best way to send a post request to a different domain using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can send a cross-domain POST request via JavaScript using the XMLHttpRequest object`s open() and send() methods.
---

**Contents**

[TOC]

#1 Using a Proxy

A proxy server can be used to send a cross-domain POST request. This involves making a request to the proxy server, which then makes the actual request to the other domain. The proxy server can then return the response back to the client.

#2 Using CORS

Cross-Origin Resource Sharing (CORS) is a mechanism that allows restricted resources on a web page to be requested from another domain outside the domain from which the resource originated. This can be done by setting the appropriate HTTP request headers and configuring the server to allow the request.

#3 Using JSONP

JSONP (JSON with Padding) is a technique used to make cross-domain requests by dynamically creating a <script> tag and adding it to the page. The script tag will then make a request to the other domain, which will return a JSON response wrapped in a function call.

#4 Using a Custom Server-Side Proxy

A custom server-side proxy can be used to make cross-domain requests. This involves setting up a proxy server on the server-side and making a request to it from the client. The proxy server can then make the actual request to the other domain and return the response back to the client.
