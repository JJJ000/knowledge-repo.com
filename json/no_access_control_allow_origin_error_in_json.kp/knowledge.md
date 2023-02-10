---
title: The requested resource does not have an 'access-control-allow-origin' header
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: This error occurs when a web page is trying to make a request to a resource from a different domain.
---

**Contents**

[TOC]

#Solution

##1. What is the 'Access-Control-Allow-Origin' Header?

The 'Access-Control-Allow-Origin' header is a response header that is used by a server to indicate which origins are allowed to access resources. It is sent in the response to a cross-origin request, and tells the browser whether or not the request should be allowed to proceed.

##2. What Causes the Error?

The 'No 'Access-Control-Allow-Origin' header is present on the requested resource' error occurs when the server does not include the 'Access-Control-Allow-Origin' header in the response to the request. This could be because the server is not configured to allow cross-origin requests, or because the server is not set up to include the header in the response.

##3. How to Fix the Error?

The 'No 'Access-Control-Allow-Origin' header is present on the requested resource' error can be fixed by configuring the server to allow cross-origin requests and to include the 'Access-Control-Allow-Origin' header in the response. This can be done by adding the appropriate configuration to the server's configuration file.

##4. Conclusion

The 'No 'Access-Control-Allow-Origin' header is present on the requested resource' error can be fixed by configuring the server to allow cross-origin requests and to include the 'Access-Control-Allow-Origin' header in the response. This can be done by adding the appropriate configuration to the server's configuration file.
