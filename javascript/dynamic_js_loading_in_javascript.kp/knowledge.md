---
title: Load JavaScript dynamically within javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is possible to dynamically load JS inside JS by using the dynamic import() syntax.
---

**Contents**

[TOC]

## Using `<script>` Tag

We can use the `<script>` tag to load a JavaScript file inside another JavaScript file.

```js
<script src="myScript.js"></script>
```

This will load the `myScript.js` file inside the current JavaScript file.

## Using `document.createElement`

We can also use the `document.createElement` method to create a `<script>` tag and set its `src` attribute to the path of the JavaScript file we want to load.

```js
const script = document.createElement('script');
script.src = 'myScript.js';
document.head.appendChild(script);
```

This will create a `<script>` tag and append it to the `<head>` element of the page, which will then load the `myScript.js` file.

## Using `fetch`

We can also use the `fetch` API to load a JavaScript file inside another JavaScript file.

```js
fetch('myScript.js')
  .then(response => response.text())
  .then(script => {
    const scriptElement = document.createElement('script');
    scriptElement.text = script;
    document.head.appendChild(scriptElement);
  });
```

This will fetch the `myScript.js` file and create a `<script>` tag with its content, which will then be appended to the `<head>` element of the page.

## Using `XMLHttpRequest`

We can also use the `XMLHttpRequest` object to load a JavaScript file inside another JavaScript file.

```js
const xhr = new XMLHttpRequest();
xhr.open('GET', 'myScript.js');
xhr.onload = function() {
  const scriptElement = document.createElement('script');
  scriptElement.text = xhr.responseText;
  document.head.appendChild(scriptElement);
};
xhr.send();
```

This will create an `XMLHttpRequest` object and use it to fetch the `myScript.js` file. It will then create a `<script>` tag with its content and append it to the `<head>` element of the page.
