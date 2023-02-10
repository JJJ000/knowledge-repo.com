---
title: Chrome will not run an ajax script because the mime type is incorrect
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Chrome will not execute an AJAX script if the MIME type of the Json is incorrect.
---

**Contents**

[TOC]

#Solution

##Cross-Origin Resource Sharing (CORS)

Chrome will refuse to execute an AJAX script due to wrong MIME type in Json if the server does not have Cross-Origin Resource Sharing (CORS) enabled. CORS is a mechanism that allows resources on a web page to be requested from another domain outside the domain from which the resource originated. This mechanism is used to protect against malicious requests and to ensure that data is not inappropriately shared between websites.

##MIME Type

In order for Chrome to accept an AJAX script, the server must have the correct MIME type set in the response header. The MIME type must be set to "application/json" for JSON data. If the MIME type is set to something else, such as "text/plain", Chrome will reject the script.

##Access-Control-Allow-Origin

In order for Chrome to execute an AJAX script with the correct MIME type, the server must also have the Access-Control-Allow-Origin header set in the response. This header must be set to "*" or the specific domain from which the request originated. If the header is not set, Chrome will reject the script.

##JSONP

If the server does not have CORS enabled, the AJAX script can still be executed by using JSONP (JSON with padding). JSONP is a technique that allows data to be requested from another domain by wrapping the JSON data in a callback function. This technique is used to bypass the same-origin policy that is enforced by browsers.
