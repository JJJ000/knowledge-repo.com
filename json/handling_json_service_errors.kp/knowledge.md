---
title: What should a JSON service return when there is an error or failure?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: A JSON service should return an error object containing a descriptive error message and an appropriate error code.
---

**Contents**

[TOC]

#### Response Format
A JSON service should return an appropriate HTTP status code, along with a JSON response body containing an error message and/or additional details about the error.

#### HTTP Status Code
The HTTP status code should indicate the type of error that occurred. Common status codes for errors include 400 (Bad Request), 401 (Unauthorized), 403 (Forbidden), 404 (Not Found), and 500 (Internal Server Error).

#### Error Message
The JSON response body should contain an error message that describes the error that occurred. This message should be human-readable, and should provide enough detail to help the user understand what went wrong.

#### Additional Details
In some cases, the JSON response body may also contain additional details about the error. This could include a unique error code, a stack trace, or a link to a page with more information about the error.
