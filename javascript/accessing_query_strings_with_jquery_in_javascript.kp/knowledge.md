---
title: Retrieve querystring from url using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: jQuery`s .attr() method can be used to retrieve querystring values from a URL.
---

**Contents**

[TOC]

## Section 1: 

Using jQuery

## Section 2:

To get the querystring from a URL using jQuery, you can use the following code:

```javascript
var queryString = window.location.search;
var params = queryString.substring(1).split('&');
var queryObj = {};

for (var i = 0; i < params.length; i++) {
  var pair = params[i].split('=');
  queryObj[pair[0]] = pair[1];
}
```

## Section 3:

The above code will parse the querystring and create an object with the key-value pairs of the querystring.

## Section 4:

You can then access the values of the querystring using the object created, e.g. `queryObj['param1']` will return the value of the `param1` parameter in the querystring.
