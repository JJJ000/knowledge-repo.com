---
title: Retrieve data after successful completion of an ajax call using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The data returned from an AJAX call can be accessed in the success callback function.
---

**Contents**

[TOC]

# Section 1: Overview

Ajax calls are a method of making asynchronous HTTP requests to a web server. These requests allow for data to be sent and received without having to reload the page. When an Ajax call is successful, the response data is returned to the client. This data can then be used to update the page or take other actions.

# Section 2: jQuery

jQuery is a JavaScript library that makes it easier to make Ajax calls. jQuery provides a number of methods for making Ajax requests, including the .ajax() method. The .ajax() method takes a number of parameters, including a success callback function. This callback function is executed when the Ajax call is successful and the response data is passed to the callback function.

# Section 3: Returning Data

The response data that is returned by the Ajax call can be accessed within the success callback function. This data can then be manipulated and used to update the page or take other actions. The data is typically returned in the form of a JavaScript object, which can be accessed using dot notation.

# Section 4: Example

For example, the following code uses the jQuery .ajax() method to make an Ajax call to a web server. The success callback function is used to access the response data and update the page with the returned data.

```
$.ajax({
  url: 'http://example.com/api/data',
  type: 'GET',
  success: function(data) {
    // Update the page with the returned data
    $('#myElement').html(data.myData);
  }
});
```
