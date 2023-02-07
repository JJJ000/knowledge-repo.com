---
title: What is the process for creating and retrieving a cookie value using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To create and read a value from a cookie with JavaScript, use the document.cookie property.
---

**Contents**

[TOC]

## Creating a Cookie

Creating a cookie in JavaScript is done by using the `document.cookie` property. This property is used to both read and write cookies.

To create a cookie, simply assign a string value to the `document.cookie` property. The string should be in the following format:

`name=value; expires=date; path=path; domain=domain; secure`

For example:

`document.cookie = "username=John Doe; expires=Thu, 18 Dec 2020 12:00:00 UTC; path=/; domain=example.com; secure"`

## Reading a Cookie

Reading a cookie in JavaScript is done by using the `document.cookie` property. This property is used to both read and write cookies.

The `document.cookie` property is a string containing a semicolon-separated list of all the cookies associated with the current document. To read a single cookie, you can use the `split()` method to break the string into an array of individual name-value pairs.

For example:

```
var cookies = document.cookie.split(';');
for (var i = 0; i < cookies.length; i++) {
  var cookie = cookies[i];
  var eqPos = cookie.indexOf('=');
  var name = eqPos > -1 ? cookie.substr(0, eqPos) : cookie;
  document.write(name + '<br>');
}
```

This code will loop through all the cookies associated with the current document, and output the name of each cookie.
