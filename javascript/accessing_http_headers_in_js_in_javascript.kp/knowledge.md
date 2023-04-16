---
title: Retrieving the http headers of a web page using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can access the web page`s HTTP Headers in JavaScript using the XMLHttpRequest object.
---

**Contents**

[TOC]

**Using the Fetch API**

The Fetch API is an interface for fetching resources, such as an HTTP request. It can be used to access the web page's HTTP headers in JavaScript.

1. Create a new `fetch` request:
    ```javascript
    fetch('url-of-the-web-page')
    ```

2. Use the `.headers` property of the `fetch` request to access the HTTP headers:
    ```javascript
    fetch('url-of-the-web-page').headers
    ```

3. Use the `.get()` method to access specific headers:
    ```javascript
    fetch('url-of-the-web-page').headers.get('header-name')
    ```

**Using the XMLHttpRequest Object**

The XMLHttpRequest object can be used to access the web page's HTTP headers in JavaScript.

1. Create a new `XMLHttpRequest` object:
    ```javascript
    let xhr = new XMLHttpRequest();
    ```

2. Open the `XMLHttpRequest` object with the `open()` method:
    ```javascript
    xhr.open('GET', 'url-of-the-web-page');
    ```

3. Use the `.getAllResponseHeaders()` method to access all the HTTP headers:
    ```javascript
    xhr.getAllResponseHeaders();
    ```

4. Use the `.getResponseHeader()` method to access specific headers:
    ```javascript
    xhr.getResponseHeader('header-name');
    ```
