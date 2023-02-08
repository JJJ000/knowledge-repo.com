---
title: There is an error with the $.ajax(...) command, as it is not a recognized function
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: $.ajax is a jQuery function, not a JSON function.
---

**Contents**

[TOC]

# Solution 1: Using jQuery

jQuery provides an easy way to make Ajax requests with the `$.ajax()` method. This method takes an object as its parameter, which contains information about the type of request, the URL to send the request to, and any data to be sent with the request.

# Solution 2: Using Fetch

If you don't want to use jQuery, you can use the Fetch API to make Ajax requests. To do this, you'll need to create a new Request object with the method, URL, and data you want to send. Then, you'll call the `fetch()` method, passing it the Request object. This will return a Promise which you can use to handle the response data.

# Solution 3: Using Axios

Another option is to use Axios, a popular library for making Ajax requests. To do this, you'll use the `axios.request()` method, passing it an object containing information about the request. This method returns a Promise which you can use to handle the response data.

# Solution 4: Using XMLHttpRequest

Finally, you can use the XMLHttpRequest API to make Ajax requests. To do this, you'll need to create a new XMLHttpRequest object, set its properties, and call the `open()` and `send()` methods. This will return a response object which you can use to handle the response data.
