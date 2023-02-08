---
title: What is the syntax for passing parameters in a get request using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Pass parameters in a GET request with jQuery by appending them to the URL as query string parameters.
---

**Contents**

[TOC]

### Passing Parameters in URL

The most straightforward method of passing parameters in a GET request with jQuery is to include them in the URL string. This can be done by appending the parameter string to the end of the URL, separated by a question mark. For example, if you wanted to pass the parameter `name` with the value `John`, the URL would be:

`https://example.com/?name=John`

### Passing Parameters as an Object

Alternatively, jQuery also allows you to pass parameters as an object. This can be done by passing an object containing the parameters as the second argument to the `$.get()` function. For example, if you wanted to pass the parameter `name` with the value `John`, the code would be:

```
$.get('https://example.com/', {
  name: 'John'
});
```

### Setting Default Parameters

You can also set default parameters in the URL string which will be used for all requests. This can be done by setting the `$.ajaxSetup()` function before making any requests. For example, if you wanted to set the default parameter `name` with the value `John`, the code would be:

```
$.ajaxSetup({
  params: {
    name: 'John'
  }
});
```

### Using `$.param()`

Finally, jQuery also provides a `$.param()` function which can be used to convert an object into a URL-encoded string. This can be useful if you need to manually construct the URL string with the parameters. For example, if you wanted to pass the parameter `name` with the value `John`, the code would be:

```
var params = {
  name: 'John'
};

var paramString = $.param(params);

// paramString = 'name=John'
```
