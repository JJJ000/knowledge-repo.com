---
title: Spring 3 mvc returns a 415 unsupported media type error when attempting to post json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The request must include a valid `Content-Type` header to be accepted by the server.
---

**Contents**

[TOC]

# Section 1: What is 415 Unsupported Media Type
415 Unsupported Media Type is an HTTP response status code indicating that the server is refusing to accept the request because the content type of the request is in an unsupported format. This error is typically returned when the server does not recognize the content type of the request. 

# Section 2: Causes of 415 Unsupported Media Type
This error can occur when a client attempts to send a request to a server using an unsupported media type. This can happen when the client is attempting to send a request with a content type that is not supported by the server. Additionally, the error may occur when the server is configured to only accept certain content types and the client is using a different one.

# Section 3: Troubleshooting 415 Unsupported Media Type
The first step in troubleshooting this error is to ensure that the client is sending the request with the correct content type. If the client is sending the request with an unsupported content type, the server will return a 415 error. Additionally, the server must be configured to accept the content type that the client is sending. This can be done by modifying the server's configuration to allow the content type that the client is sending.

# Section 4: Conclusion
In conclusion, a 415 Unsupported Media Type error is an HTTP response status code indicating that the server is refusing to accept the request because the content type of the request is in an unsupported format. This error can occur when a client attempts to send a request to a server using an unsupported media type. To troubleshoot this error, the client should ensure that the request is being sent with the correct content type and the server should be configured to accept the content type that the client is sending.
