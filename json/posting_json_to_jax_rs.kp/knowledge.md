---
title: What is the process for sending a JSON object to a jax-rs service?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Send a POST request with the JSON object as the body of the request.
---

**Contents**

[TOC]

### Step 1: Create a JSON Object

Create a JSON object using a language of your choice. For example, in JavaScript, you can use the `JSON.stringify` method to convert a JavaScript object into a JSON string.

```javascript
let jsonObj = {
    "name": "John Doe",
    "age": 30
};
let jsonString = JSON.stringify(jsonObj);
```

### Step 2: Create an HTTP Request

Create an HTTP request with the POST method. Set the header to `Content-Type: application/json` and include the JSON string as the body of the request.

```javascript
let request = new XMLHttpRequest();
request.open('POST', 'http://example.com/api/resource', true);
request.setRequestHeader('Content-Type', 'application/json');
request.send(jsonString);
```

### Step 3: Handle the Response

Handle the response from the server. The response will contain the data returned by the JAX-RS service.

```javascript
request.onload = function() {
    if (request.status >= 200 && request.status < 400) {
        let response = JSON.parse(request.responseText);
        // do something with the response
    } else {
        // handle errors
    }
};
```

### Step 4: Error Handling

If the request fails, handle the error. Check the status code of the response to determine the cause of the error.

```javascript
request.onerror = function() {
    // handle errors
};
```
