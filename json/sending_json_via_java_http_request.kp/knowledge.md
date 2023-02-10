---
title: Sending a post request using Java httpurlconnection with JSON data
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: To send a POST request with JSON data using Java HttpUrlConnection, set the request body to the JSON string and set the `Content-Type` header to `application/json`.
---

**Contents**

[TOC]

### Section 1: Making the Request

Making the request with a Java HttpUrlConnection is simple. First, create an HttpUrlConnection object:

```java
URL url = new URL("http://example.com/api/endpoint");
HttpURLConnection connection = (HttpURLConnection) url.openConnection();
```

Then set the request method to POST and set the Content-Type header to application/json:

```java
connection.setRequestMethod("POST");
connection.setRequestProperty("Content-Type", "application/json");
```

### Section 2: Sending the Data

Next, you need to set the request body. To do this, you need to open an output stream and write the data to it:

```java
connection.setDoOutput(true);
DataOutputStream outputStream = new DataOutputStream(connection.getOutputStream());
outputStream.writeBytes(jsonString);
outputStream.flush();
outputStream.close();
```

Where `jsonString` is the string representation of the JSON data you want to send.

### Section 3: Reading the Response

Once you have sent the data, you can read the response from the server. To do this, you need to open an input stream and read the response from it:

```java
InputStream inputStream = connection.getInputStream();
BufferedReader reader = new BufferedReader(new InputStreamReader(inputStream));
String response = reader.readLine();
```

The `response` variable will contain the response from the server.

### Section 4: Closing the Connection

Finally, you need to close the connection:

```java
connection.disconnect();
```
