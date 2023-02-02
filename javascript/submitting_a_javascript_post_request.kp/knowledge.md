---
title: Submitting a JavaScript request similar to a form submission
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A JavaScript post request can be sent using the XMLHttpRequest object`s open() and send() methods.
---

**Contents**

[TOC]

**Using XHR**

XMLHttpRequest (XHR) is an API available to web browsers that can be used to send HTTP requests. XHR can be used to send a POST request, similar to a form submission, with the data encoded in the body of the request.

**Constructing the Request**

To construct the request, an XMLHttpRequest object must be created and configured. The request type should be set to 'POST' and the URL of the request should be set to the form's action attribute. The body of the request should be set to the form data, which can be done by setting the send() method's parameter to a string of the form data encoded in the appropriate format (e.g. application/x-www-form-urlencoded).

**Sending the Request**

Once the request is configured, it can be sent by calling the send() method with the form data as the parameter. The response from the server can then be handled by setting an onload callback function to the XMLHttpRequest object.

**Handling the Response**

The response from the server can be handled by setting an onload callback function to the XMLHttpRequest object. The response data can be accessed through the responseText property of the XMLHttpRequest object. The response data can then be parsed and used as needed.
