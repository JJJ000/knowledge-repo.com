---
title: Send an okhttp request with a JSON body
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The body of an OkHttp POST request can be specified as a JSON object.
---

**Contents**

[TOC]

1. Setting Up the Request Body

To set up the request body, you need to create a JSONObject and add the necessary key-value pairs to it. For example, if you wanted to send a POST request with a JSON body containing the key “name” and the value “John Doe”, you would do the following:

```
JSONObject jsonObject = new JSONObject();
jsonObject.put("name", "John Doe");
```

2. Creating the Request

Once the JSONObject is created, you can then create the request using the OkHttp library. To do this, you need to create a RequestBody object and then set the content type to JSON.

```
RequestBody body = RequestBody.create(JSON, jsonObject.toString());
Request request = new Request.Builder()
  .url("http://www.example.com")
  .post(body)
  .build();
```

3. Executing the Request

Finally, you can execute the request using the OkHttp library. To do this, you need to create an OkHttpClient object and then call the newCall() method on it.

```
OkHttpClient client = new OkHttpClient();
Response response = client.newCall(request).execute();
```

4. Parsing the Response

Once the request is executed, you can parse the response using the OkHttp library. To do this, you need to call the body() method on the Response object and then use the fromJson() method to parse the response.

```
String responseString = response.body().string();
JSONObject responseJson = new JSONObject(responseString);
```
