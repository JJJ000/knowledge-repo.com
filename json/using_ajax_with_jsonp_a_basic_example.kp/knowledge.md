---
title: What is an example of using .ajax() with jsonp?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: $.ajax({url `example.com/data?callback=?`, dataType `jsonp`});
---

**Contents**

[TOC]

#Section 1: Setup

Before using .ajax() with JSONP, it is important to set up the request correctly. This includes setting the dataType to "jsonp" and setting the type to "GET".

#Section 2: Sending the Request

Once the request is set up correctly, the .ajax() method can be used to send the request. The URL of the request must be specified, as well as the callback parameter, which is the name of the function that will be called when the response is received.

#Section 3: Handling the Response

When the response is received, the callback function specified in the request is called. This function will receive the data from the response as an argument. This data can then be processed as needed.

#Section 4: Example

Here is an example of using .ajax() with JSONP:

$.ajax({
  url: 'http://example.com/jsonp',
  dataType: 'jsonp',
  type: 'GET',
  data: {
    param1: 'value1',
    param2: 'value2'
  },
  jsonp: 'callback',
  success: function(data) {
    // Process data here
  }
});
