---
title: Attempting to utilize fetch and input the mode no-cors
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Fetch with mode no-cors can be used to make requests to a server that doesn`t support CORS.
---

**Contents**

[TOC]

1. What is Fetch?
Fetch is an API that allows you to make network requests in the browser. It is a modern replacement for XMLHttpRequest (XHR). It's an easier way to make requests for data from a server and get a response back.

2. What is Mode: no-cors?
Mode: no-cors is an option that can be passed into the Fetch API. This mode prevents the request from being made with the credentials of the user, such as cookies or HTTP authentication. It also prevents the response from being exposed to the application, so the response will not contain any of the data requested.

3. Why Use Fetch and Mode: no-cors?
Fetch and Mode: no-cors can be used when making requests to a server that does not support CORS (Cross-Origin Resource Sharing). This is useful when the server does not support CORS and the data requested needs to be kept private.

4. How to Use Fetch and Mode: no-cors in JavaScript?
Using Fetch and Mode: no-cors in JavaScript is very simple. All you need to do is call the fetch() method, passing in the URL of the resource you want to request, and then pass in an options object with the mode set to 'no-cors'. For example:

fetch('http://example.com/data.json', {
  mode: 'no-cors'
})
.then(response => {
  // Do something with the response
});
