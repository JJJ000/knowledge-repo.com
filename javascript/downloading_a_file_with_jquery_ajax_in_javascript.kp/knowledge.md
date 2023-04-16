---
title: Retrieve a file using jquery.ajax
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery.ajax() can be used to download a file by making an asynchronous HTTP (Ajax) request.
---

**Contents**

[TOC]

##Section 1: Setting up the jQuery.Ajax Request

jQuery.Ajax is a powerful tool for making asynchronous HTTP requests. To download a file using jQuery.Ajax, you will need to set up a request object with the URL of the file you want to download, the HTTP method (GET or POST), and any additional parameters or data that you wish to include in the request.

```javascript
var request = {
    url: 'http://example.com/file.zip',
    type: 'GET',
    data: {
        param1: 'value1',
        param2: 'value2'
    }
};
```

##Section 2: Making the jQuery.Ajax Call

Once the request object is set up, you can make the jQuery.Ajax call. The call should include a success and error callback, so that you can handle the response appropriately.

```javascript
$.ajax(request)
    .done(function(data, textStatus, jqXHR) {
        //success callback
    })
    .fail(function(jqXHR, textStatus, errorThrown) {
        //error callback
    });
```

##Section 3: Handling the Response

In the success callback, you can access the response data and use it to download the file. Depending on the server-side configuration, the response may be a binary file, a JSON object, or a text string.

If the response is a binary file, you can use the [FileSaver.js library](https://github.com/eligrey/FileSaver.js/) to save the file to the user's computer.

If the response is a JSON object or text string, you can parse the data and use it to generate the file.

##Section 4: Example

Here is an example of how to download a file using jQuery.Ajax. This example assumes that the server is sending back a binary file in the response.

```javascript
//set up the request object
var request = {
    url: 'http://example.com/file.zip',
    type: 'GET',
    data: {
        param1: 'value1',
        param2: 'value2'
    }
};

//make the jQuery.Ajax call
$.ajax(request)
    .done(function(data, textStatus, jqXHR) {
        //use FileSaver.js to save the file
        saveAs(data, 'file.zip');
    })
    .fail(function(jqXHR, textStatus, errorThrown) {
        //handle the error
    });
```
