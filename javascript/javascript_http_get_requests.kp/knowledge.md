---
title: How to make an http get request using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A GET request in JavaScript can be made using the XMLHttpRequest object`s open() and send() methods.
---

**Contents**

[TOC]

#### XMLHttpRequest
The most common way to make a GET request in JavaScript is to use the `XMLHttpRequest` object. This object is supported in all major browsers and provides a simple, standardized way to make a request.

```javascript
var xhr = new XMLHttpRequest();
xhr.open('GET', 'http://www.example.com/data.json');
xhr.send();
```

#### Fetch API
The `fetch` API is a newer, more modern way to make a GET request in JavaScript. It is supported in all major browsers and provides a more concise syntax than the `XMLHttpRequest` object.

```javascript
fetch('http://www.example.com/data.json')
  .then(response => response.json())
  .then(data => console.log(data))
```

#### jQuery
The jQuery library also provides a way to make a GET request in JavaScript. The `$.get()` method is a shorthand for making a GET request with jQuery.

```javascript
$.get('http://www.example.com/data.json', function(data) {
  console.log(data);
});
```

#### Axios
Axios is a popular JavaScript library for making HTTP requests. It is supported in all major browsers and provides a simple syntax for making a GET request.

```javascript
axios.get('http://www.example.com/data.json')
  .then(response => console.log(response.data))
```
