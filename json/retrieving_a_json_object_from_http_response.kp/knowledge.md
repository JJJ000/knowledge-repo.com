---
title: Retrieve a JSON object from an http response
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The JSON object can be retrieved from the HTTP response by deserializing the response body into a JSON object.
---

**Contents**

[TOC]

### Using JavaScript

Using JavaScript, you can parse a JSON object from a HTTP response by using the `JSON.parse()` method. This method takes a string as a parameter and returns a JavaScript object.

```javascript
// Get the response from the HTTP request
let response = http.get('http://example.com/api/data');

// Parse the JSON object from the response
let json = JSON.parse(response);
```

### Using jQuery

Using jQuery, you can parse a JSON object from a HTTP response by using the `$.getJSON()` method. This method takes a URL as a parameter and returns a JavaScript object.

```javascript
// Get the JSON object from the URL
$.getJSON('http://example.com/api/data', function(json) {
  // Use the JSON object here
});
```

### Using Node.js

Using Node.js, you can parse a JSON object from a HTTP response by using the `require('request')` module. This module takes a URL as a parameter and returns a JavaScript object.

```javascript
// Require the request module
const request = require('request');

// Get the JSON object from the URL
request('http://example.com/api/data', function(error, response, body) {
  // Parse the JSON object from the response
  let json = JSON.parse(body);
});
```

### Using Python

Using Python, you can parse a JSON object from a HTTP response by using the `json` module. This module takes a string as a parameter and returns a Python dictionary.

```python
# Get the response from the HTTP request
response = http.get('http://example.com/api/data')

# Parse the JSON object from the response
json = json.loads(response)
```
