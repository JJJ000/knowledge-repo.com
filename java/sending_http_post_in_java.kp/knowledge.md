---
title: Submitting an http post request using java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To send an HTTP POST request in Java, use the HttpURLConnection class to open a connection and use the setDoOutput(true) method to enable output.
---

**Contents**

[TOC]

### 1. Creating The Request

To create an HTTP POST request in Java, you will need to create an instance of the `HttpPost` class. This class is a subclass of the `HttpEntityEnclosingRequestBase` class, which is used to make requests that contain an entity body.

The `HttpPost` class takes in two parameters: the URL of the request and an `HttpEntity` object. The `HttpEntity` object is used to represent the request body and can be created using the `StringEntity` class.

### 2. Setting The Headers

To set the headers of the request, you will need to create an instance of the `HttpHeaders` class. This class provides methods for setting the headers of the request.

The `HttpHeaders` class also provides methods for setting the content type and content length of the request.

### 3. Executing The Request

Once the request has been created and the headers have been set, you can execute the request using the `execute` method of the `HttpClient` class. This method takes in the `HttpPost` object as a parameter and returns an `HttpResponse` object.

The `HttpResponse` object contains the response code, headers, and body of the response.

### 4. Handling The Response

Finally, you will need to handle the response. Depending on the type of response, you may need to parse the response body or read the response code.

To parse the response body, you can use the `EntityUtils` class. This class provides methods for parsing the response body into a `String` or `JSONObject`.

To read the response code, you can use the `getStatusCode` method of the `HttpResponse` object. This method returns an `int` value that represents the response code.
