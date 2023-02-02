---
title: What is the best way to use jquery to upload files asynchronously?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: jQuery can be used to upload files asynchronously by using the $.ajax() method.
---

**Contents**

[TOC]

## HTML Form

The first step to uploading files asynchronously with jQuery is to create an HTML form with an `<input>` tag of type `file`. This will allow the user to select the file they wish to upload.

## jQuery AJAX

Next, use jQuery's `$.ajax()` method to send the file data to the server. This method takes an object as an argument, which should include the URL of the server, the type of request (`POST` in this case), and the data to be sent (the file).

## FormData

To send the file data to the server, it must be wrapped in a `FormData` object. This object can be created using the `new FormData()` constructor, and the file data can be added using the `append()` method. 

## Callback Function

Finally, a callback function should be passed to the `$.ajax()` method. This function will be executed when the AJAX request is complete, and can be used to handle the response from the server.
