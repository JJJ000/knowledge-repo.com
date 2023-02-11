---
title: What is the syntax for receiving a JSON response using system.net.webrequest in c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the `GetResponseStream()` method to get the JSON response from the System.Net.WebRequest object.
---

**Contents**

[TOC]

### Section 1: Create WebRequest

To create a WebRequest, you need to use the `System.Net.WebRequest.Create` method. You should pass the URL of the resource you want to request as a parameter.

```csharp
WebRequest request = WebRequest.Create("http://example.com/data.json");
```

### Section 2: Set Request Method

Once you have created the WebRequest, you need to set the request method. This is the type of HTTP request you want to make (e.g. GET, POST, PUT, etc.). In this case, you want to make a GET request.

```csharp
request.Method = "GET";
```

### Section 3: Get Response

Once you have set the request method, you can get the response from the server. This will return a `WebResponse` object.

```csharp
WebResponse response = request.GetResponse();
```

### Section 4: Read Response Stream

The response will contain a stream of data. To read this data, you need to use the `StreamReader` class. This will allow you to read the response as a string.

```csharp
using (StreamReader reader = new StreamReader(response.GetResponseStream()))
{
    string responseString = reader.ReadToEnd();
}
```

Once you have the response as a string, you can parse it as JSON using a JSON library such as Newtonsoft.Json.
