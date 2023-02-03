---
title: What is the purpose of the 'access-control-allow-origin' header?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The Access-Control-Allow-Origin header is used to indicate which domains are allowed to access resources from a server.
---

**Contents**

[TOC]

#### What is the 'Access-Control-Allow-Origin' Header?
The `Access-Control-Allow-Origin` header is an HTTP response header that is used to indicate whether a resource on a web server can be accessed by a web page from a different origin (domain). This header is used by browsers to determine whether a cross-origin request is allowed or not. 

#### When is the 'Access-Control-Allow-Origin' Header Used?
The `Access-Control-Allow-Origin` header is used when a web page on one domain attempts to make a request to a resource on another domain. This header is used to indicate which domains are allowed to make cross-origin requests.

#### How Does the 'Access-Control-Allow-Origin' Header Work?
The `Access-Control-Allow-Origin` header works by allowing the server to specify which domains can make a cross-origin request. If the server includes this header in its response, the browser will allow the request to be made from the specified domain. If the header is not included, the request will be blocked. 

#### What Are the Different Values for the 'Access-Control-Allow-Origin' Header?
The `Access-Control-Allow-Origin` header can be set to either a single domain (e.g. `example.com`) or the wildcard value `*` which indicates that all domains are allowed to make a cross-origin request.
