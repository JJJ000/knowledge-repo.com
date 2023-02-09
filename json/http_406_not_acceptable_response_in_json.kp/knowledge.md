---
title: What does the http error code '406 - not acceptable response' mean?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: `406-Not Acceptable Response` in HTTP is a response status code indicating that the server cannot produce a response in a format acceptable to the client.
---

**Contents**

[TOC]

# Overview

The HTTP 406 Not Acceptable response status code indicates that the server cannot produce a response matching the list of acceptable values specified in the request's "Accept" header. This is usually because the requested resource is only capable of generating a response entity which is not acceptable according to the accept headers sent in the request.

# Causes

The most common cause of a 406 Not Acceptable response is when the client sends an Accept header containing a media type which the server is unable to generate a response for. For example, if the client sends an Accept header of "application/json", but the server is only capable of generating a response entity in HTML, then the server will return a 406 Not Acceptable response.

# Solutions

The client can modify the Accept header to include media types which the server is capable of generating a response for. For example, if the client sends an Accept header of "application/json", but the server is only capable of generating a response entity in HTML, then the client should modify the Accept header to include "text/html".

The server can also modify its response to include media types which the client is capable of accepting. For example, if the client sends an Accept header of "application/json", but the server is only capable of generating a response entity in HTML, then the server can modify the response to include a "Content-Type" header with a value of "application/json".
