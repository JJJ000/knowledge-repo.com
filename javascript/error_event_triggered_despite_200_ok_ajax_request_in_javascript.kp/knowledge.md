---
title: Despite the ajax request returning a status of 200 ok, an error event was triggered instead of a success event
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The response may not be valid JSON, or the response may indicate an error in the response body.
---

**Contents**

[TOC]

# Possible Causes
1. The response body contains an error message.
2. The server is not configured to return a successful response.
3. The response contains an unexpected status code.
4. The response is malformed.

# Troubleshooting
1. Check the response body for an error message.
2. Check the server configuration to make sure it is configured to return a successful response.
3. Check the response for an unexpected status code.
4. Check the response for any malformed data.

# Resolution
1. If the response body contains an error message, then the issue should be addressed with the server configuration.
2. If the server is not configured to return a successful response, then it should be reconfigured to do so.
3. If the response contains an unexpected status code, then it should be corrected.
4. If the response is malformed, then it should be corrected.
