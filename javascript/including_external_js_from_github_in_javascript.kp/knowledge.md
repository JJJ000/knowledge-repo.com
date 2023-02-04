---
title: Include and run a JavaScript file located on github
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use a <script> tag with a src attribute set to the URL of the external JavaScript file hosted on GitHub to link and execute the external JavaScript file.
---

**Contents**

[TOC]

## Method 1: Using a Script Tag 

The easiest way to include an external JavaScript file hosted on GitHub is to use a script tag in the HTML document. The script tag should include the URL of the file on GitHub, as well as the type of script being included.

```html
<script src="https://github.com/path/to/file.js" type="text/javascript"></script>
```

## Method 2: Using ajax 

Another way to include an external JavaScript file hosted on GitHub is to use an AJAX request. This can be done by creating a new XMLHttpRequest object and setting the URL of the file on GitHub as the open method's parameter.

```javascript
var xhttp = new XMLHttpRequest();
xhttp.open("GET", "https://github.com/path/to/file.js", true);
xhttp.send();
```

## Method 3: Using Fetch API 

The Fetch API can also be used to include an external JavaScript file hosted on GitHub. This can be done by creating a new Request object and setting the URL of the file on GitHub as the parameter.

```javascript
fetch("https://github.com/path/to/file.js")
    .then(response => response.text())
    .then(text => eval(text));
```

## Method 4: Using jQuery 

The jQuery library also provides an easy way to include an external JavaScript file hosted on GitHub. This can be done by using the getScript method and passing the URL of the file on GitHub as the parameter.

```javascript
$.getScript("https://github.com/path/to/file.js");
```
