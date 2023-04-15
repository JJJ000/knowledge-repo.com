---
title: When using jquery, it is not possible to load a url through xmlhttprequest
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This error occurs when the web browser blocks the XMLHttpRequest due to the Same-Origin Policy.
---

**Contents**

[TOC]

# Problem description

When using jQuery to make an XMLHttpRequest in order to retrieve JSON data from a certain URL, an error occurs and the request fails. The error message returned by the browser console is:

`XMLHttpRequest cannot load <URL>. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin <origin> is therefore not allowed access.`


# Explanation

This error message indicates that the problem is related to the Same-Origin Policy enforced by the browser. This policy restricts web pages from making requests to a different domain, port or protocol than the one used to serve the web page itself. This is a security measure designed to prevent cross-site scripting attacks and data leakage between sites.

In this case, the XMLHttpRequest sent by jQuery is attempting to access a resource located in a different domain or port than the one used to serve the web page, and the server hosting the resource is not configured to allow cross-origin requests. Therefore, the browser blocks the request and returns an error.


# Solution

To overcome this issue, the server hosting the JSON resource needs to add the appropriate headers to its response in order to allow cross-origin requests. Specifically, it needs to include the `Access-Control-Allow-Origin` header, which specifies the domains or origins that are allowed to make requests to the resource.

If you don't have access to the server, you can use a proxy server or a server-side script to retrieve the data and pass it to the client-side code. Alternatively, you can use a JSONP request, which uses a script tag to load the data and bypasses the Same-Origin Policy.


# Example

Here's an example of how to use JSONP with jQuery:

```
$.ajax({
  url: '<URL>',
  dataType: 'jsonp',
  success: function(data) {
    console.log(data);
  },
  error: function(jqXHR, textStatus, errorThrown) {
    console.log('Error:', errorThrown);
  }
});
```

This code sends a JSONP request to the specified URL, which returns data wrapped in a callback function. jQuery automatically generates a unique name for the callback function, appends it to the URL and sets the `dataType` option to `jsonp`. Once the data is retrieved, the `success` callback is called with the data as a parameter. If an error occurs, the `error` callback is called with the error message.
