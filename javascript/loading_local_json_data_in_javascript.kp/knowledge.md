---
title: Retrieving a JSON file from the local system
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the fetch API or XMLHttpRequest to load the local JSON file.
---

**Contents**

[TOC]

## Loading JSON File

To load a local JSON file, you can use the `fetch()` API in modern browsers:

```javascript
fetch('my_data.json')
  .then(response => response.json())
  .then(data => console.log(data));
```

The `fetch()` API is a modern way to make HTTP requests and is supported by most modern browsers.

## Using XMLHttpRequest

Alternatively, you can use the `XMLHttpRequest` API to make an HTTP request for the JSON file:

```javascript
var xhr = new XMLHttpRequest();
xhr.open('GET', 'my_data.json', true);
xhr.onload = function () {
  var data = JSON.parse(xhr.responseText);
  console.log(data);
};
xhr.send();
```

The `XMLHttpRequest` API is an older way to make HTTP requests, but is still widely supported by browsers.

## Using jQuery

If you are using jQuery, you can use the `$.getJSON()` method to make an HTTP request for the JSON file:

```javascript
$.getJSON('my_data.json', function(data) {
  console.log(data);
});
```

## Using Node.js

If you are using Node.js, you can use the `fs` module to read the JSON file:

```javascript
const fs = require('fs');
const data = fs.readFileSync('my_data.json');
const jsonData = JSON.parse(data);
console.log(jsonData);
```
