---
title: Making an http request to a server with a JSON payload and receiving a JSON response in return, without using the jquery library
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the XMLHttpRequest object to send a JSON to the server and receive a JSON response in return.
---

**Contents**

[TOC]

### Sending a JSON

Sending a JSON to a server can be done through the use of the `XMLHttpRequest` object. This object allows for asynchronous communication between a client and server. The following code snippet demonstrates how to send a JSON object to a server:

```javascript
var jsonObject = {
  name: "John Doe",
  age: 22
};

// Create a new XMLHttpRequest object
var xhr = new XMLHttpRequest();

// Set the request type and URL
xhr.open("POST", "https://example.com/endpoint", true);

// Set the Content-Type header
xhr.setRequestHeader("Content-Type", "application/json");

// Send the JSON object
xhr.send(JSON.stringify(jsonObject));
```

### Retrieving a JSON

Retrieving a JSON from a server can also be done through the use of the `XMLHttpRequest` object. The following code snippet demonstrates how to receive a JSON object from a server:

```javascript
// Create a new XMLHttpRequest object
var xhr = new XMLHttpRequest();

// Set the request type and URL
xhr.open("GET", "https://example.com/endpoint", true);

// Set the onload handler
xhr.onload = function() {
  if (xhr.readyState === 4 && xhr.status === 200) {
    // Parse the JSON response
    var jsonObject = JSON.parse(xhr.responseText);
  }
};

// Send the request
xhr.send();
```

### Error Handling

It is important to handle errors when sending and retrieving JSON data. The `XMLHttpRequest` object has an `onerror` handler that can be used to handle errors. The following code snippet demonstrates how to handle errors when sending and receiving a JSON object:

```javascript
// Create a new XMLHttpRequest object
var xhr = new XMLHttpRequest();

// Set the request type and URL
xhr.open("POST", "https://example.com/endpoint", true);

// Set the Content-Type header
xhr.setRequestHeader("Content-Type", "application/json");

// Set the onload handler
xhr.onload = function() {
  if (xhr.readyState === 4 && xhr.status === 200) {
    // Parse the JSON response
    var jsonObject = JSON.parse(xhr.responseText);
  }
};

// Set the onerror handler
xhr.onerror = function() {
  console.error("An error occurred");
};

// Send the JSON object
xhr.send(JSON.stringify(jsonObject));
```
