---
title: How to return a string as JSON in an mvc architecture
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Return a string as JSON by using the json\_encode() function.
---

**Contents**

[TOC]

**Section 1: Create a JSON String**

To return a string as JSON in Java, you must first create a JSON string. This can be done by creating a JSONObject and adding the desired string as a key-value pair. For example, to return the string "Hello World" as JSON, you could create a JSONObject like this:

```
JSONObject jsonObject = new JSONObject();
jsonObject.put("message", "Hello World");
```

**Section 2: Convert to a String**

Once you have created the JSONObject, you must convert it to a string. This can be done using the toString() method of the JSONObject class. The resulting string will be a valid JSON string representing the object. For example, the following code will convert the jsonObject we created in the previous section to a string:

```
String jsonString = jsonObject.toString();
```

**Section 3: Return the JSON String**

To return the JSON string, you must use a response object to send it back to the client. This can be done using the ResponseEntity class, which allows you to set the response body, status code, and other response headers. For example, the following code will return the jsonString we created in the previous section:

```
return ResponseEntity.ok().body(jsonString);
```

**Section 4: Handle the Response**

On the client side, the response must be handled appropriately. This depends on the type of client making the request. For example, if the client is a web browser, the response can be handled by setting the response type to "application/json" and parsing the response body as JSON.
