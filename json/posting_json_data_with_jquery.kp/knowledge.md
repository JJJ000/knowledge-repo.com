---
title: What is the best way to post JSON data using jquery?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can use the jQuery.ajax() method to post JSON data.
---

**Contents**

[TOC]

1. Include JQuery Library

In order to use JQuery for posting JSON data, the JQuery library must first be included in the HTML page. This can be done by adding the following code in the `<head>` section of the page:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```

2. Create AJAX Request

Once the JQuery library is included, an AJAX request can be created with the `$.ajax()` method. This method takes an object as an argument, which can be used to define the request properties. The `type` property should be set to `"POST"` and the `data` property should be set to a JSON string:

```javascript
$.ajax({
  type: "POST",
  data: JSON.stringify(data),
  contentType: "application/json; charset=utf-8",
  dataType: "json"
});
```

3. Set URL and Callback

The `url` property of the AJAX request should be set to the URL of the API endpoint. The `success` property should be set to a callback function that will be called when the request is successful:

```javascript
$.ajax({
  type: "POST",
  data: JSON.stringify(data),
  contentType: "application/json; charset=utf-8",
  dataType: "json",
  url: "http://example.com/api/endpoint",
  success: function(responseData) {
    // Do something with the response
  }
});
```

4. Send Request

Finally, the AJAX request can be sent with the `$.ajax()` method:

```javascript
$.ajax({
  type: "POST",
  data: JSON.stringify(data),
  contentType: "application/json; charset=utf-8",
  dataType: "json",
  url: "http://example.com/api/endpoint",
  success: function(responseData) {
    // Do something with the response
  }
}).done(function() {
  // Do something after the request is complete
});
```
