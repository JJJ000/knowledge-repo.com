---
title: How can I use ajax to send JSON data with jquery?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the jQuery.ajax() method with the type option set to `PUT` and the data option set to the JSON string.
---

**Contents**

[TOC]

### Section 1: Prepare Data

Before sending a JSON object to the server, you need to prepare the data. This can be done using the `JSON.stringify()` method. This method will take a JavaScript object and convert it into a JSON string that can be sent to the server.

### Section 2: Send Request

Once the data is prepared, you can use jQuery's `$.ajax()` method to send the request. This method takes a URL, the type of request (PUT in this case), and the data to be sent.

### Section 3: Handle Response

Once the request is sent, you can use the `$.ajax()` method's `success` callback to handle the response from the server. This response will be a JSON object that can be parsed using the `JSON.parse()` method.

### Section 4: Use Data

Once the response is parsed, you can use the data in your application. This could include displaying it on the page, saving it to a database, etc.
