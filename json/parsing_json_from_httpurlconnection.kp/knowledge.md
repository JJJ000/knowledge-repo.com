---
title: Extract JSON data from an httpurlconnection object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The HttpURLConnection object can be parsed into a JSON object using the JSONObject class.
---

**Contents**

[TOC]

**Section 1: Create HttpURLConnection Object**

The first step is to create a HttpURLConnection object to make a request to the URL that contains the JSON. This can be done using the URL class and the openConnection() method:

```java
URL url = new URL("http://example.com/json");
HttpURLConnection connection = (HttpURLConnection) url.openConnection();
```

**Section 2: Set Request Method**

The next step is to set the request method for the connection. This is typically done by calling the setRequestMethod() method on the HttpURLConnection object:

```java
connection.setRequestMethod("GET");
```

**Section 3: Make Request**

Once the request method is set, the request can be made by calling the connect() method on the HttpURLConnection object:

```java
connection.connect();
```

**Section 4: Parse JSON Response**

Finally, the response can be parsed using a JSON library such as Gson. The response can be read from the InputStream of the HttpURLConnection object:

```java
InputStream inputStream = connection.getInputStream();
Gson gson = new Gson();
MyObject myObject = gson.fromJson(inputStream, MyObject.class);
```
