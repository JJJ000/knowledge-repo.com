---
title: What is the syntax for sending JSON data in an http request using nsurlrequest?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Send the JSON data as the request body of the NSURLRequest using the HTTPBody property.
---

**Contents**

[TOC]

### Section 1: Create NSURLRequest

Create an instance of NSURLRequest with the URL of the endpoint you want to send the data to.

### Section 2: Set Request Body

Set the body of the request to the JSON data you want to send. To do this, use the `setValue:forHTTPHeaderField:` method on the NSMutableURLRequest instance and set the content type to `application/json`.

### Section 3: Set Request Method

Set the request method to `POST` if you want to send the data to the server.

### Section 4: Send Request

Send the request using the `sendAsynchronousRequest:queue:completionHandler:` method on the `NSURLConnection` class.
