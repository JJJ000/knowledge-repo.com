---
title: Send a JSON object via an http post request
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Send the JSON data as the body of the HTTP POST request.
---

**Contents**

[TOC]

## Section 1: Setting Up the Request

To pass JSON data to an HTTP POST request, the first step is to create an HTTP request object. This can be done with the `XMLHttpRequest` object in JavaScript.

Once the request object is created, the `open` method can be used to open a connection to the desired URL, along with the method type (in this case, `POST`) and the `true` parameter to indicate that the request should be asynchronous.

## Section 2: Setting the Header

The next step is to set the request header. This is done with the `setRequestHeader` method, which takes two parameters: the header name (in this case, `Content-Type`) and the value (`application/json`).

## Section 3: Sending the Data

Once the header is set, the JSON data can be sent with the `send` method. This takes one parameter, which is the data that should be sent with the request.

## Section 4: Processing the Response

Finally, the response can be processed with the `onreadystatechange` event handler. This event is triggered when the request is complete, and the response can be accessed through the `responseText` property of the request object.
