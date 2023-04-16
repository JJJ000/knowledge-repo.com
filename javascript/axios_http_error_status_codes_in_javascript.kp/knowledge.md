---
title: What is the process for obtaining the status code from an http error in axios?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get the status code from an HTTP error in Axios by accessing the `response.status` property of the error object.
---

**Contents**

[TOC]

### Using Axios

Using Axios, you can access the status code of an HTTP error in the `response.status` property of the error object. For example:

```javascript
axios.get('/user/12345')
  .catch(function (error) {
    if (error.response) {
      // The request was made and the server responded with a status code
      // that falls out of the range of 2xx
      console.log(error.response.status);
    }
  });
```

### Using Fetch

Using the Fetch API, you can access the status code of an HTTP error in the `status` property of the response object. For example:

```javascript
fetch('/user/12345')
  .then(function(response) {
    if (!response.ok) {
      // response.status is the status code
      console.log(response.status);
    }
  }).catch(function(error) {
    console.log(error);
  });
```
