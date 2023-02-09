---
title: Error 415 unsupported media type when using json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The 415 Unsupported Media Type error indicates that the server is refusing to accept the request due to an unsupported media type, such as a request containing an unsupported format of JSON.
---

**Contents**

[TOC]

# Section 1: What is HTTP 415?
HTTP 415 is an HTTP status code that indicates that the server is refusing to accept the request because the content type of the request is not supported.

# Section 2: What is JSON?
JSON (JavaScript Object Notation) is a text-based data interchange format used to represent structured data. It is a lightweight, language-independent data format that is easy to read and write.

# Section 3: What Causes a HTTP 415 Error?
A HTTP 415 error occurs when a server receives a request that has a content type that is not supported. This could be due to the server not recognizing the content type, or the content type not being supported by the server.

# Section 4: How to Fix a HTTP 415 Error with JSON?
To fix a HTTP 415 error with JSON, the server needs to be configured to accept the content type of the request. This can be done by adding the appropriate MIME type to the server configuration. Additionally, the client should ensure that the content type of the request is set correctly.
