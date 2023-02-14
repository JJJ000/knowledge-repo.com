---
title: Make an http request to get a JSON object in nodejs
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: You can use the built-in `http` module in NodeJS to make an HTTP request and get a JSON response.
---

**Contents**

[TOC]

# Making the Request

Making an HTTP request in Node.js is done using the [`http` module](https://nodejs.org/api/http.html). The `http.get()` method is the most common way to make a request.

```js
const http = require('http');

http.get('http://example.com/data.json', (res) => {
  const { statusCode } = res;
  const contentType = res.headers['content-type'];

  let error;
  if (statusCode !== 200) {
    error = new Error('Request Failed.\n' +
                      `Status Code: ${statusCode}`);
  } else if (!/^application\/json/.test(contentType)) {
    error = new Error('Invalid content-type.\n' +
                      `Expected application/json but received ${contentType}`);
  }
  if (error) {
    console.error(error.message);
    // consume response data to free up memory
    res.resume();
    return;
  }

  res.setEncoding('utf8');
  let rawData = '';
  res.on('data', (chunk) => { rawData += chunk; });
  res.on('end', () => {
    try {
      const parsedData = JSON.parse(rawData);
      console.log(parsedData);
    } catch (e) {
      console.error(e.message);
    }
  });
}).on('error', (e) => {
  console.error(`Got error: ${e.message}`);
});
```

# Parsing the Response

Once the request is complete, the response data needs to be parsed into a usable JavaScript object. This can be done using the [`JSON.parse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse) method.

```js
res.on('end', () => {
  try {
    const parsedData = JSON.parse(rawData);
    console.log(parsedData);
  } catch (e) {
    console.error(e.message);
  }
});
```

# Error Handling

Error handling is an important part of making an HTTP request. The response object can be checked for errors, such as a non-200 status code or an invalid content type.

```js
let error;
if (statusCode !== 200) {
  error = new Error('Request Failed.\n' +
                    `Status Code: ${statusCode}`);
} else if (!/^application\/json/.test(contentType)) {
  error = new Error('Invalid content-type.\n' +
                    `Expected application/json but received ${contentType}`);
}
if (error) {
  console.error(error.message);
  // consume response data to free up memory
  res.resume();
  return;
}
```
