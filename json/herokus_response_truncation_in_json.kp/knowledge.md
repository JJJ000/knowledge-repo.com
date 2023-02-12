---
title: Does heroku shorten http responses?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, Heroku truncates HTTP responses in Json to prevent large responses from overloading the server.
---

**Contents**

[TOC]

##### Yes
Heroku has been known to truncate HTTP responses in Json. This is done as a security measure, as it prevents malicious scripts from executing on the server.

##### How
Heroku truncates HTTP responses in Json by limiting the maximum length of the response. If the response is longer than the maximum length, Heroku will truncate the response and return an error.

##### Impact
The truncation of HTTP responses in Json can have a significant impact on applications. It can cause errors or unexpected behavior, as some applications rely on the full response to function properly.

##### Solutions
Fortunately, there are ways to work around Heroku's truncation of HTTP responses in Json. One solution is to compress the response using gzip, which can reduce the length of the response and prevent it from being truncated. Another solution is to use chunked transfer encoding, which allows the response to be sent in chunks, preventing it from being truncated.
