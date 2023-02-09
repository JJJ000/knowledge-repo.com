---
title: What is the syntax for sending JSON data instead of a query string using $.ajax?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `data` option to specify the data to send as a JSON object.
---

**Contents**

[TOC]

1. Building the JSON Object
--------------------------------
The JSON object can be built using JavaScript's native `JSON.stringify()` method. This method takes a JavaScript object as an argument and returns a JSON string. For example:

```javascript
var data = {
    name: "John Smith",
    age: 30
};

var jsonData = JSON.stringify(data);
```

2. Configuring the AJAX Request
--------------------------------
Once the JSON object is built, the `$.ajax()` method can be used to send the request. The `data` option should be set to the JSON string, and the `contentType` should be set to `"application/json; charset=utf-8"`. For example:

```javascript
$.ajax({
    type: "POST",
    url: "/some/url",
    data: jsonData,
    contentType: "application/json; charset=utf-8",
    dataType: "json"
});
```

3. Sending the Request
-----------------------
Finally, the AJAX request can be sent by calling the `$.ajax()` method. For example:

```javascript
$.ajax();
```
