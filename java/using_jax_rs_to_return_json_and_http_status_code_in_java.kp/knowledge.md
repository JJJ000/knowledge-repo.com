---
title: What is the best way to return both JSON data and an http status code using jax-rs?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Return a Response object with the desired status code and entity containing the JSON data.
---

**Contents**

[TOC]

1. Overview

AJAX-RS is a Java API for creating RESTful web services. It allows a developer to easily create web services that are accessible from any client that supports the HTTP protocol. One of the key features of AJAX-RS is the ability to return both JSON and HTTP status codes together in a single response.

2. Using Response

The Response class is the primary class used for returning JSON and HTTP status codes together in AJAX-RS. It is a generic class that can be used to return any type of response. To return JSON and an HTTP status code together, the Response class must be initialized with the desired status code and the JSON object.

3. Example

Below is an example of how to use the Response class to return JSON and an HTTP status code together.

```
// Create a JSON object
JSONObject jsonObject = new JSONObject();
jsonObject.put("name", "John Doe");

// Create a Response object with the desired status code and the JSON object
Response response = Response.status(200).entity(jsonObject).build();

// Return the Response object
return response;
```

4. Conclusion

Using the Response class in AJAX-RS is an easy and efficient way to return both JSON and HTTP status codes together in a single response. This makes it easy for developers to create web services that are accessible from any client that supports the HTTP protocol.
