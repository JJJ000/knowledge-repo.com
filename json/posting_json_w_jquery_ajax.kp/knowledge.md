---
title: Sending JSON data via jquery ajax to a web service
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, jQuery Ajax can be used to post JSON data to a web service in JSON format.
---

**Contents**

[TOC]

1. What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is designed to be easily readable and writable for humans and machines. JSON is language-independent, meaning it can be used in any programming language.

2. How to Post JSON Data with jQuery
Posting JSON data with jQuery is relatively straightforward. First, you must create a JavaScript object containing the data you want to send to the server. Then, you use the jQuery $.ajax() method to send an HTTP POST request to the web service, with the JSON data as the request body.

3. Example
The following example shows how to post JSON data with jQuery:

```javascript
var data = {
    "name": "John Doe",
    "age": 25
};

$.ajax({
    url: "http://example.com/webservice",
    type: "POST",
    contentType: "application/json; charset=utf-8",
    data: JSON.stringify(data),
    dataType: "json",
    success: function(response) {
        // do something with the response
    }
});
```

4. Conclusion
Posting JSON data with jQuery is a straightforward process. You must first create a JavaScript object containing the data you want to send to the server, then use the jQuery $.ajax() method to send an HTTP POST request to the web service, with the JSON data as the request body.
