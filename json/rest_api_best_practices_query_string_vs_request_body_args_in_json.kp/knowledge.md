---
title: Best practices for using query strings and request bodies in a rest api
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: It is generally recommended to use a query string for simple arguments and a request body in JSON for more complex arguments.
---

**Contents**

[TOC]

# Arguments in Query Strings

When sending arguments in query strings, the arguments are appended to the end of the URL and are visible in the address bar of the browser. This makes it easier to debug and inspect the request. Additionally, query strings are easier to construct and read, making them easier to use and maintain.

# Arguments in Request Body

When sending arguments in the request body, they are hidden from the user and are not visible in the address bar. This can be beneficial when sending sensitive data like passwords or API keys. Additionally, request bodies can be used to send complex data like arrays and objects, which cannot be sent in a query string.
