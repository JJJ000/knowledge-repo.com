---
title: Sending data to an $http.get request using angularjs
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `params` property of the configuration object passed to $http.get() to pass data to the request.
---

**Contents**

[TOC]

1. Overview

AngularJS provides a simple way to pass data to an HTTP request using the $http service. This is done by adding the data as a parameter to the $http.get() method. The data can be either an object or a string.

2. Syntax

The syntax for passing data to an $http.get() request is as follows:

$http.get(url, {params: data});

Where:

• url – The URL of the request
• data – The data to be passed in the request

3. Examples

Let's say we have a web service that returns a list of users from a database. We can pass the search criteria as a parameter to the $http.get() request.

// Get list of users
$http.get('/users', {params: {name: 'John'}})
    .then(function(response) {
        // Handle response
    });

In this example, we are passing the parameter name with the value ‘John’ to the /users endpoint.

4. Conclusion

Using the $http service, it is easy to pass data to an HTTP request in AngularJS. This is done by adding the data as a parameter to the $http.get() method. The data can be either an object or a string.
