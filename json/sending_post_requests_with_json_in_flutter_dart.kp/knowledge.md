---
title: Sending an http post request with a JSON body using flutter/dart
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the http package`s post() method, passing in the desired url, body data in JSON format, and headers.
---

**Contents**

[TOC]

## Step 1: Setting up the Request

In order to make an HTTP POST request with a JSON body, the first step is to create a `HttpClient` object and a `Uri` object. The `HttpClient` object will be used to make the request and the `Uri` object will contain the URL of the endpoint the request will be sent to. 

```dart
var httpClient = HttpClient();
var uri = Uri.parse("http://example.com/endpoint");
```

## Step 2: Creating the Request

Once the `HttpClient` and `Uri` objects have been created, the next step is to create the actual request. This can be done by calling the `HttpClient.postUrl` method and passing in the `Uri` object as an argument.

```dart
var request = await httpClient.postUrl(uri);
```

## Step 3: Adding the JSON Body

Once the request has been created, the next step is to add the JSON body. This can be done by calling the `HttpClientRequest.write` method and passing in the JSON string as an argument.

```dart
var jsonString = {
  "name": "John Doe",
  "age": 42
};

request.write(jsonString);
```

## Step 4: Sending the Request

Finally, the request can be sent by calling the `HttpClientRequest.close` method. This will return a `Future<HttpClientResponse>` object which can be used to access the response from the endpoint.

```dart
var response = await request.close();
```
