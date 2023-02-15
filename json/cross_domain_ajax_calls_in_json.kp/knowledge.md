---
title: Making an ajax request to a different domain
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: AJAX cross domain calls in JSON are not possible due to same-origin policy restrictions.
---

**Contents**

[TOC]

# Section 1: What is AJAX Cross Domain Call
AJAX cross domain call is a technique used to make requests to a different domain than the one the page is currently on. This technique is used to bypass the same-origin policy, which restricts access to resources from different domains.

# Section 2: Benefits of AJAX Cross Domain Call
AJAX cross domain call offers a number of advantages when compared to traditional methods of making requests. It allows for faster loading times, since the request is made asynchronously, and it also allows for more secure data transfer, since the data is not passed through the browser.

# Section 3: How to Make an AJAX Cross Domain Call
Making an AJAX cross domain call is relatively easy. The first step is to create a script tag that contains the URL of the request. This script tag should also include a callback parameter that will be called when the request is complete. After the script tag is created, the JavaScript code can be written to make the request.

# Section 4: JSON and AJAX Cross Domain Call
JSON is a popular format for data transfer and is often used with AJAX cross domain calls. To make an AJAX cross domain call using JSON, the request should include a header that specifies the data type as JSON. The response should also be in JSON format. The JSON data can then be parsed and used in the JavaScript code.
