---
title: What is JSONP (json with padding)?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-14 00:00:00
updated_at: 2023-01-14 00:00:00
tldr: JSONP is a technique used to bypass the same-origin policy by wrapping JSON data in a function call, allowing it to be requested from a different domain.
---

**Contents**

[TOC]

### What is JSONP

JSONP (JSON with Padding) is a technique used to bypass the same-origin policy, which prevents JavaScript code from making requests to a different domain than the one from which it was served. JSONP works by dynamically creating a `<script>` tag in the HTML document and setting its src attribute to a URL that returns JSON-formatted data wrapped in a function call.

### Why was it created

JSONP was created to allow web applications to access data from different domains. This is necessary because of the same-origin policy, which prevents JavaScript code from making requests to a different domain than the one from which it was served. JSONP solves this problem by dynamically creating a `<script>` tag in the HTML document and setting its src attribute to a URL that returns JSON-formatted data wrapped in a function call. This allows the web application to receive data from a different domain while still being able to execute the code.
