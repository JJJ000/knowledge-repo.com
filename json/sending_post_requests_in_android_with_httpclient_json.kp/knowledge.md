---
title: What is the process for sending a post request in JSON format via httpclient in an Android device?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the HttpClient.post() method to send a POST request in JSON format using HTTPClient in Android.
---

**Contents**

[TOC]

## 1. Adding Dependency

In order to use the `HttpClient` library in your Android project, you will need to add the following dependency to your `build.gradle` file:

```
implementation 'org.apache.httpcomponents:httpclient:4.5.12'
```

## 2. Creating an HttpClient Instance

Once the dependency is added, you can create an `HttpClient` instance and use it to make your request.

```java
HttpClient httpclient = new DefaultHttpClient();
```

## 3. Setting Up the Request

To set up the request, you will need to create a `HttpPost` instance and set the request body to a `StringEntity` containing the JSON data.

```java
HttpPost httppost = new HttpPost("http://example.com/path/to/api");
StringEntity requestBody = new StringEntity("{\"key\":\"value\"}");
httppost.setEntity(requestBody);
```

## 4. Executing the Request

Finally, you can execute the request by calling `HttpClient.execute` and passing it the `HttpPost` instance.

```java
HttpResponse response = httpclient.execute(httppost);
```
