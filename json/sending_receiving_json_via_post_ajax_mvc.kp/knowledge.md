---
title: Make an ajax post request with JSON data and get a JSON response back from the mvc controller
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Send an AJAX POST request to the Controller, passing the JSON data as the request body, and receive a JSON response from the Controller.
---

**Contents**

[TOC]

**Section 1: Sending JSON Data via POST**

Using the jQuery library, you can send a JSON object to a controller in an MVC framework using an ajax call. The following example shows how to do this:

```javascript
$.ajax({
    type: "POST",
    url: "controller/action",
    data: JSON.stringify({
        param1: "value1",
        param2: "value2"
    }),
    contentType: "application/json; charset=utf-8",
    dataType: "json",
    success: function(data) {
        // Do something with the response
    }
});
```

**Section 2: Receiving JSON Response from Controller**

To receive a JSON response from the controller, you will need to set the dataType of the ajax call to "json". Then, the response from the controller will automatically be parsed into a JavaScript object.

The following example shows how to do this:

```javascript
$.ajax({
    type: "POST",
    url: "controller/action",
    data: JSON.stringify({
        param1: "value1",
        param2: "value2"
    }),
    contentType: "application/json; charset=utf-8",
    dataType: "json",
    success: function(data) {
        // Do something with the response
    }
});
```

In the success function of the ajax call, the data parameter will contain the JSON response from the controller. This data can then be used to update the page or take other actions.
