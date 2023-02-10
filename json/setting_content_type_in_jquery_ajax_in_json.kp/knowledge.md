---
title: It is not possible to specify the content-type as 'application/json' when using jquery.ajax()
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, jQuery.ajax does not support setting the content-type to `application/json`.
---

**Contents**

[TOC]

# Answer

## Setting Content-Type
The content-type header is used to indicate the media type of the resource. It is generally used in the context of an HTTP request or response. jQuery does not provide a way to set the content-type header directly. However, it can be done indirectly by setting the dataType option to 'json'. This will set the content-type header to 'application/json'.

## jQuery.ajax
jQuery.ajax is a method used to make asynchronous HTTP requests. It allows the user to specify various options such as the URL, data, type of request, and success and error callbacks. It does not provide a way to directly set the content-type header, but it can be done indirectly by setting the dataType option to 'json'.

## Example
The following example shows how to set the content-type header to 'application/json' using jQuery.ajax:

```javascript
$.ajax({
    url: 'example.com/api/v1/data',
    type: 'GET',
    dataType: 'json',
    success: function(data) {
        // Do something with the data
    }
});
```

## Conclusion
In conclusion, it is not possible to set the content-type header directly in jQuery.ajax, but it can be done indirectly by setting the dataType option to 'json'. This will set the content-type header to 'application/json'.
