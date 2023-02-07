---
title: Making a fetch get request with a query string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can set a query string in a Fetch GET request by passing an object as the second argument containing the query parameters.
---

**Contents**

[TOC]

### Step 1: Define the URL

The first step is to define the URL for the request. This will include the endpoint and any query string parameters.

```javascript
const url = 'https://example.com/api?param1=value1&param2=value2';
```

### Step 2: Create the Request

Next, create a new Request object and pass in the URL.

```javascript
const request = new Request(url);
```

### Step 3: Make the Request

Finally, make the request using the fetch() method.

```javascript
fetch(request)
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log(error));
```

### Step 4: Handle the Response

Once the request is made, handle the response by using the .then() and .catch() methods. The .then() method is used to handle the successful response and the .catch() method is used to handle any errors.
