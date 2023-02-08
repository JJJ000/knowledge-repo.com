---
title: What is the process for accessing and reading a local JSON file using javascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the `fetch()` API to read an external local JSON file in JavaScript.
---

**Contents**

[TOC]

1. **Create an XMLHttpRequest Object**
In order to read the external JSON file, you must first create an XMLHttpRequest object. This is a JavaScript object that allows you to make HTTP requests to an external server.

2. **Open the JSON File**
Once the XMLHttpRequest object has been created, you can open the JSON file by setting the open() method of the object. The open() method takes three parameters: the type of request (GET or POST), the URL of the file, and a boolean value indicating whether the request should be asynchronous or not.

3. **Send the Request**
Once the open() method has been called, the request can be sent using the send() method. This method takes no parameters and simply sends the request to the server.

4. **Process the Response**
Once the response has been received, the responseText property of the XMLHttpRequest object can be used to access the contents of the file. The responseText property contains the response as a string, which can then be parsed using the JSON.parse() method. This method takes the string as a parameter and returns a JavaScript object.
