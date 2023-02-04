---
title: Submit post information via xmlhttprequest
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Send an XMLHttpRequest with the POST method and include the data in the request body.
---

**Contents**

[TOC]

### Creating the Request

The XMLHttpRequest object can be used to send POST data to a server. To create a request, you must first instantiate a new XMLHttpRequest object:

```javascript
var xhr = new XMLHttpRequest();
```

### Setting the Request Type

Next, you must set the request type to `POST` and specify the URL of the server endpoint:

```javascript
xhr.open("POST", "http://example.com/endpoint");
```

### Building the Request Data

The data to be sent to the server should be built as a string and stored in a variable:

```javascript
var data = "key1=value1&key2=value2";
```

### Sending the Request

Finally, the request can be sent using the `send()` method, passing the data as an argument:

```javascript
xhr.send(data);
```
