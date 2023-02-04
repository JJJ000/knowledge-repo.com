---
title: What is the process for sending formdata objects using ajax requests with jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the jQuery.ajax() method and specify the dataType as `FormData`.
---

**Contents**

[TOC]

## Constructing the FormData Object

The FormData object is used to construct a set of key/value pairs which represent form fields and their values. It can be constructed using the `FormData` constructor:

```javascript
var formData = new FormData();
```

You can then append values to the FormData object using the `append` method:

```javascript
formData.append('fieldName', 'fieldValue');
```

## Sending the FormData Object with jQuery

Once the FormData object has been constructed, it can be sent with an Ajax request using jQuery's `$.ajax()` method:

```javascript
$.ajax({
  url: 'http://example.com/api/upload',
  type: 'POST',
  data: formData,
  processData: false,
  contentType: false
});
```

The `processData` and `contentType` options are set to `false` to prevent jQuery from attempting to process the FormData object.

## Handling the Response

The response from the Ajax request can be handled using the `success` callback:

```javascript
$.ajax({
  url: 'http://example.com/api/upload',
  type: 'POST',
  data: formData,
  processData: false,
  contentType: false,
  success: function(data) {
    // Handle the response here
  }
});
```

## Error Handling

The `error` callback can be used to handle any errors that occur during the Ajax request:

```javascript
$.ajax({
  url: 'http://example.com/api/upload',
  type: 'POST',
  data: formData,
  processData: false,
  contentType: false,
  error: function(xhr, status, error) {
    // Handle the error here
  }
});
```
