---
title: Recording data with retrofit 2
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Retrofit 2 can be used to log HTTP request and response data for debugging purposes by using the HttpLoggingInterceptor class.
---

**Contents**

[TOC]

### Introduction

Retrofit is a type-safe HTTP client for Android and Java. It is a popular library for making network requests, and it is used in many popular applications. Retrofit makes it easy to make requests and receive responses from web services. It also provides a powerful logging feature that allows developers to log requests and responses.

### Setting Up Logging

To enable logging with Retrofit, you need to add the logging interceptor to the Retrofit builder. This interceptor will log the request and response information for each request made. The logging interceptor can be added like this:

```
Retrofit retrofit = new Retrofit.Builder()
    .baseUrl(BASE_URL)
    .addConverterFactory(GsonConverterFactory.create())
    .client(client)
    .addInterceptor(new HttpLoggingInterceptor().setLevel(HttpLoggingInterceptor.Level.BODY))
    .build();
```

### Logging Levels

When setting up the logging interceptor, you can also specify the logging level. The logging level determines what information will be logged. The available levels are:

- NONE: No logging
- BASIC: Logs request and response information
- HEADERS: Logs request and response information, as well as request and response headers
- BODY: Logs request and response information, as well as request and response bodies

### Logging Output

Once the logging interceptor is set up, the request and response information will be logged. The logging output will look something like this:

```
--> POST https://example.com/api/v1/users
Content-Type: application/json; charset=UTF-8
Content-Length: 37

{"name":"John Doe","age":20}

<-- 200 OK https://example.com/api/v1/users
Content-Type: application/json; charset=UTF-8
Content-Length: 37

{"name":"John Doe","age":20}
```
