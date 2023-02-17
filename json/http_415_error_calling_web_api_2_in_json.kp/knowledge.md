---
title: An error of 'http 415 unsupported media type' is encountered when attempting to access a web API 2 endpoint
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The 415 error indicates that the server cannot process the requested content type, which in this case is JSON.
---

**Contents**

[TOC]

# Overview
The HTTP 415 Unsupported Media Type error is an HTTP status code that indicates that the server is unable to process the request due to an unsupported media type. This error can occur when calling a Web API 2 endpoint in JSON.

# Causes
The HTTP 415 Unsupported Media Type error can occur when the content type of the request body is not supported by the server. This can happen when the client sends a request with a Content-Type header set to a media type that is not supported by the server. For example, if the server only supports application/json and the client sends a request with a Content-Type header set to application/xml, the server will return a 415 error.

# Solutions
The most common solution to this problem is to ensure that the client is sending a request with a Content-Type header set to a media type that is supported by the server. In the example above, the client should set the Content-Type header to application/json.

If the client is using an HTTP client library, it may be necessary to configure the library to set the correct Content-Type header. For example, in the .NET HttpClient library, the DefaultRequestHeaders.Accept property can be used to set the Content-Type header.
