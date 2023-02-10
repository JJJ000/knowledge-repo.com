---
title: Send data in jsonp format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: AJAX requests can be used to post data to a JSONP endpoint.
---

**Contents**

[TOC]

1. What is JSONP?
2. How to Post Data to a JSONP Endpoint?
3. Pros and Cons of JSONP
4. Alternatives to JSONP

## 1. What is JSONP?
JSONP (JSON with Padding) is a technique used to bypass the same-origin policy, which prevents JavaScript code from making requests to a different domain than the one from which it originated. JSONP works by dynamically creating a <script> tag in the page, which points to a URL on the remote domain, and adds a parameter to the URL that contains the name of a callback function. The remote server then returns a response containing the JavaScript code for the callback function, along with the requested data, which is passed as an argument to the callback function.

## 2. How to Post Data to a JSONP Endpoint?
Posting data to a JSONP endpoint is relatively straightforward. The first step is to create a <script> tag in the page with the URL of the endpoint, along with any query parameters that need to be passed. The second step is to add a parameter to the URL that contains the name of a callback function. The third step is to define the callback function, which will be called when the response is received. Finally, the fourth step is to make sure that the callback function is called with the data that was requested.

## 3. Pros and Cons of JSONP
The primary benefit of using JSONP is that it allows data to be requested from a different domain, which would normally be prohibited by the same-origin policy. This is especially useful for web applications that need to access data from external sources.

However, JSONP also has some drawbacks. For example, it is not secure, as the data is passed in plain text, and it is not possible to use HTTP headers for authentication. Additionally, JSONP is limited to GET requests, and it is not possible to use other HTTP methods such as POST, PUT, and DELETE.

## 4. Alternatives to JSONP
If the same-origin policy needs to be bypassed, but JSONP is not an option, there are a few alternatives. One option is to use a proxy server, which can be used to make requests to a remote domain and then return the response to the original domain. Another option is to use CORS (Cross-Origin Resource Sharing), which is a mechanism that allows web applications to make requests to a different domain. Finally, it is also possible to use an iframe to make requests to a different domain.
