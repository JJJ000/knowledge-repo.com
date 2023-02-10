---
title: What is the process of sending a JSON request using apache httpclient?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the Apache HttpClient`s HttpPost method and set the entity as a StringEntity containing the JSON request body.
---

**Contents**

[TOC]

# Section 1: Creating the JSON Request

Creating a JSON request using Apache HttpClient is relatively straightforward. The first step is to create a JSON object that contains the data that you would like to send. This can be done using the `org.json` library. For example:

```java
JSONObject json = new JSONObject();
json.put("name", "John Doe");
json.put("age", 42);
```

# Section 2: Creating an HttpPost Request

Once the JSON object has been created, the next step is to create an HttpPost request. This can be done using the `org.apache.http.client.methods.HttpPost` class. The URL of the endpoint should be specified in the constructor of the class. The JSON object should then be added to the request as an entity using the `setEntity()` method.

```java
HttpPost request = new HttpPost("http://example.com/endpoint");
StringEntity params = new StringEntity(json.toString());
request.addHeader("content-type", "application/json");
request.setEntity(params);
```

# Section 3: Executing the Request

The request can then be executed using the `org.apache.http.client.HttpClient` class. The `execute()` method should be used to execute the request and the response can be retrieved using the `getEntity()` method.

```java
HttpClient httpClient = HttpClientBuilder.create().build();
HttpResponse response = httpClient.execute(request);
String responseString = EntityUtils.toString(response.getEntity(), "UTF-8");
```

# Section 4: Parsing the Response

The response can then be parsed using the `org.json` library. This can be done by creating a new `JSONObject` object and passing the response string to it.

```java
JSONObject responseJson = new JSONObject(responseString);
```

The response can then be accessed using the `get()` method. For example, if the response contains a field called `message` then it can be retrieved like so:

```java
String message = responseJson.get("message");
```
