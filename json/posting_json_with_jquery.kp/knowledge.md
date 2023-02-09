---
title: Sending valid JSON in the request body using jquery
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, jQuery can post valid JSON in the request body.
---

**Contents**

[TOC]

**Section 1 - What is JSON?**

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is human-readable text that is used to transmit data objects consisting of attribute-value pairs and array data types. It is commonly used for asynchronous browser-server communication, including as an alternative to XML in Ajax web applications.

**Section 2 - How to Post JSON using jQuery?**

jQuery provides the $.post() method for sending data to a server. This method allows us to send an AJAX request with JSON data in the request body. To do this, we need to set the contentType option to application/json and the data option to a valid JSON string.

**Section 3 - Example of Posting JSON with jQuery**

Below is an example of a jQuery AJAX call using the $.post() method to send JSON data in the request body.

```javascript
$.ajax({
  type: "POST",
  url: "/some/url",
  contentType: "application/json",
  data: JSON.stringify({
    "foo": "bar"
  }),
  success: function(data) {
    // Do something with the response data
  }
});
```

**Section 4 - Benefits of Posting JSON with jQuery**

Posting JSON with jQuery provides several benefits. It allows for more efficient communication between the client and server, as JSON is a lighter alternative to XML. It also makes it easier to work with complex data, as it can be easily parsed and manipulated on the client-side. Finally, it is a more secure way of sending data, as it eliminates the need to send sensitive data in the URL.
