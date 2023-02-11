---
title: Post requests are not reaching the rest API if the data is in JSON format, but they do reach the API if the data is in xml format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The server is not configured to accept JSON data in a POST request.
---

**Contents**

[TOC]

## Introduction

HTTP status code 415 Unsupported Media Type is an error code that indicates that the server is unable to process the request because the content type of the request is not supported. In this case, the POST request is not reaching the REST endpoint if the content type is JSON, but it does if the content type is XML. This section will explain why this is happening and how to solve the problem.

## Reasons for Error

The most likely cause of this error is that the server is not configured to accept requests with a JSON content type. This means that when the client sends a POST request with a JSON content type, the server is unable to process it and returns the error code 415 Unsupported Media Type.

Another possible cause of this error is that the server is not configured to accept requests with the correct content type. For example, if the server is configured to accept requests with an XML content type but the client sends a request with a JSON content type, the server will return the error code 415 Unsupported Media Type.

## Solutions

The first solution is to configure the server to accept requests with the correct content type. For example, if the server is configured to accept requests with an XML content type, then the client should send a request with an XML content type.

The second solution is to configure the server to accept requests with a JSON content type. This can be done by adding the following line to the server's configuration:

`AddType application/json .json`

The third solution is to use a different content type for the request. For example, if the server is configured to accept requests with an XML content type, then the client can use an XML content type for the request.

## Conclusion

In conclusion, the error code 415 Unsupported Media Type occurs when the server is unable to process the request because the content type of the request is not supported. The most likely cause of this error is that the server is not configured to accept requests with the correct content type. To solve this problem, the server should be configured to accept requests with the correct content type or a different content type can be used for the request.
