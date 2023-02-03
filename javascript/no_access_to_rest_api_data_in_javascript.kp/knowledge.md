---
title: The requested resource does not have an 'access-control-allow-origin' header, preventing access to data from a rest api
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The request cannot be completed due to a lack of CORS permissions.
---

**Contents**

[TOC]

**What is the 'Access-Control-Allow-Origin' Header?**

The 'Access-Control-Allow-Origin' header is an HTTP response header that defines which origin (domain) is allowed to access a resource. It is used to allow cross-origin requests, such as those made by a web browser using XMLHttpRequest, in web applications.

**Why is the 'Access-Control-Allow-Origin' Header Important?**

The 'Access-Control-Allow-Origin' header is important because it helps prevent cross-site request forgery (CSRF) attacks. It also helps to ensure that only authorized domains can access the requested resource.

**What Happens When No 'Access-Control-Allow-Origin' Header is Present?**

When no 'Access-Control-Allow-Origin' header is present, the browser will not allow the request to be made. This means that the request will fail and the requested resource will not be retrieved.

**How Can the 'Access-Control-Allow-Origin' Header be Added?**

The 'Access-Control-Allow-Origin' header can be added to the response from the server by setting the response header to the domain that is allowed to access the resource. For example, if the domain 'www.example.com' is allowed to access the resource, the response header should be set to 'Access-Control-Allow-Origin: www.example.com'.
