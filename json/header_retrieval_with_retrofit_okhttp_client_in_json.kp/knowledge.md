---
title: Retrieving the response header (using retrofit or okhttp client)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To get the header from a response using Retrofit/OkHttp client in JSON format, you can call the response.header() method and pass in the header string key as a parameter.
---

**Contents**

[TOC]

## Retrofit and OkHttp Clients

Retrofit is a type-safe HTTP client for Android and Java, and OkHttp is an HTTP client that supports HTTP/2 and SPDY. Together, they are commonly used to build robust network applications. 

## Response Headers

HTTP response headers are used to provide information about the server, the response content and cache controls. In some cases, applications may need to use the headers for their operations. Retrieving response headers from a Retrofit client is a straightforward process.

## Retrieving Response Headers

To retrieve response headers, one of the ways is to use the `Headers` annotation in the Retrofit client interface. For example, to retrieve the `Content-Type` header, the following code snippet can be used:

```
@GET("/example")
@Headers("Content-Type: application/json")
Call<ResponseBody> getExample();
```

Once the response is received in the form of a `ResponseBody` object, the headers can be retrieved by calling the `headers()` method of the `Response` object. For example, to retrieve the `Content-Type` header, the following code snippet can be used:

```
Call<ResponseBody> call = retrofitClient.getExample();
Response<ResponseBody> response = call.execute();

if(response.isSuccessful()) {
  Headers headers = response.headers();
  String contentType = headers.get("Content-Type");
}
```

This will retrieve the `Content-Type` header from the response.

## Conclusion

Retrieving headers from a response in Retrofit and OkHttp clients is a straightforward process. The `Headers` annotation can be used to retrieve headers from the server, and the `headers()` method can be used to retrieve them from the `Response` object.
