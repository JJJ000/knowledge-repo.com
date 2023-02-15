---
title: The content type of the JSON requestbody in a spring rest post request is not supported
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: The Content-Type header of the request should be set to application/json.
---

**Contents**

[TOC]

### Section 1: Overview

When making a REST API call, the request body must be in a format that is supported by the API. If a request body is sent in a format that is not supported, the API will return an error.

### Section 2: Common Formats

The most common formats for sending a request body are JSON and XML. Both of these formats are widely used and supported by most APIs.

### Section 3: Content Type

When sending a request body, the content type must also be specified. The content type tells the API what format the request body is in. For example, if the request body is in JSON format, the content type should be “application/json”.

### Section 4: Troubleshooting

If the API returns an error stating that the content type is not supported, it is likely that the content type specified in the request is incorrect. Check the content type to ensure that it matches the format of the request body.
