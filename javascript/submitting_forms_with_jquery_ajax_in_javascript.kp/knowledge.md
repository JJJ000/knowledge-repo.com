---
title: Send a form with jquery ajax
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: jQuery can be used to submit a form using AJAX in Javascript by calling the jQuery.ajax() or jQuery.post() method.
---

**Contents**

[TOC]

**Section 1: jQuery Selectors**

jQuery selectors are used to select elements in the DOM (Document Object Model). This allows us to access and manipulate elements in the page. The basic syntax for a jQuery selector is $(selector).

**Section 2: jQuery AJAX**

jQuery AJAX is a method of making asynchronous HTTP requests from the client side. It allows us to send data to the server and receive a response without reloading the page. The basic syntax for a jQuery AJAX call is $.ajax(url, settings).

**Section 3: Submitting a Form**

To submit a form using jQuery AJAX, we first need to select the form element using a jQuery selector. Then we can call the $.ajax() function, passing in the URL of the form's action, as well as any additional settings.

**Section 4: Example Code**

Here is an example of how to submit a form using jQuery AJAX:

```javascript
$('#myForm').submit(function(e) {
    e.preventDefault(); // Prevent the default form submission
    $.ajax({
        url: $(this).attr('action'), // Get the URL of the form's action
        type: 'POST', // Set the request type to POST
        data: $(this).serialize(), // Serialize the form data
        success: function(data) {
            // Handle the success callback
        }
    });
});
```
