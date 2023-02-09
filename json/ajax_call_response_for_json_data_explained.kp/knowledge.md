---
title: What does the format of an ajax call response 'for (;;); { JSON data }' signify?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: This is a security measure used to protect against XSS attacks, where the `for (;;);` part is used to indicate that the response should be ignored, and the `{ JSON data }` is the actual response data.
---

**Contents**

[TOC]

## Definition

"For (;;);" is a JavaScript construct used to prevent a malicious user from accessing data from an Ajax call. It is commonly used to return JSON data from the server to the client.

## Use

When an Ajax call is made, the server will respond with a string of data that includes a "for (;;);" prefix. The client-side JavaScript code will then strip off the prefix and parse the remaining JSON data.

## Benefits

The use of this construct helps to prevent cross-site scripting (XSS) attacks. By prefixing the JSON data with "for (;;);", malicious users are unable to access the data directly, as the JavaScript code will not execute the prefix.

## Limitations

The use of this construct does not guarantee protection against XSS attacks. Other security measures, such as input validation and output encoding, should also be implemented to ensure data security.
