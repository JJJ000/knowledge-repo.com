---
title: Including a header in an httpurlconnection
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can add a header to an HttpURLConnection in Java by using the setRequestProperty() method.
---

**Contents**

[TOC]

### Setting the Request Method

The request method is set using the `setRequestMethod()` method. The valid request methods are `GET`, `POST`, `HEAD`, `OPTIONS`, `PUT`, `DELETE`, `TRACE`.

### Setting the Request Headers

The request headers are set using the `setRequestProperty()` method. This method takes two parameters, the header field and the value. For example, to set the `Content-Type` header to `application/json`, the code would look like this:

```java
connection.setRequestProperty("Content-Type", "application/json");
```

### Adding Custom Request Headers

It is also possible to add custom request headers. To do this, the `addRequestProperty()` method can be used. This method takes two parameters, the header field and the value. For example, to add a `X-My-Header` header with value `MyValue`, the code would look like this:

```java
connection.addRequestProperty("X-My-Header", "MyValue");
```

### Setting the User-Agent Header

The User-Agent header is used to identify the type of browser and operating system being used by the client. To set the User-Agent header, the `setRequestProperty()` method can be used. For example, to set the User-Agent header to `Mozilla/5.0`, the code would look like this:

```java
connection.setRequestProperty("User-Agent", "Mozilla/5.0");
```
