---
title: What could cause an error event instead of a successful event when an AJAX request returns a status code of 200 OK?
authors:
- cool_wizard
tags:
- ajax
- javascript
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The response might not be in the correct format for the JSON parser to read.
---

**Contents**

[TOC]

### Overview 
When an AJAX request returns a status of 200 OK, it should fire a success event, not an error event. This issue can be caused by a number of different issues, including incorrect response headers, incorrect response data, or an issue with the browser or server. 

### Incorrect Response Headers
The response headers sent back from the server can sometimes cause an issue with the success or failure of an AJAX request. If the response headers are not properly configured, the browser may interpret the response as an error, even if the status code is 200 OK. To resolve this issue, the server should be configured to send the proper response headers for the request.

### Incorrect Response Data
If the data sent back from the server is not valid JSON, the browser will not be able to interpret it correctly. This can cause the browser to interpret the response as an error, even if the status code is 200 OK. To resolve this issue, the server should be configured to send valid JSON data in the response.

### Browser or Server Issue
Sometimes, the issue can be caused by a bug in the browser or server. In this case, the best solution is to update the browser or server to the latest version to ensure that any known bugs are fixed.
