---
title: How can I make a post request in c# to send a JSON and get the JSON response?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Send an HttpWebRequest with a JSON string as the request body and receive the response as a JSON string.
---

**Contents**

[TOC]

### Sending JSON via POST

Using the `HttpWebRequest` class, it is possible to send a POST request to a web service with a JSON body.

The following code example shows how to send a POST request with a JSON body to a web service:

```csharp
string url = "http://example.com/api/endpoint";

var httpWebRequest = (HttpWebRequest)WebRequest.Create(url);
httpWebRequest.ContentType = "application/json";
httpWebRequest.Method = "POST";

using (var streamWriter = new StreamWriter(httpWebRequest.GetRequestStream()))
{
    string json = "{\"key\":\"value\"}";

    streamWriter.Write(json);
    streamWriter.Flush();
    streamWriter.Close();
}

var httpResponse = (HttpWebResponse)httpWebRequest.GetResponse();
using (var streamReader = new StreamReader(httpResponse.GetResponseStream()))
{
    var responseText = streamReader.ReadToEnd();
    // ...
}
```

### Receiving JSON

The response from the web service can be read from the `HttpWebResponse` object.

The following code example shows how to read the JSON response from the web service:

```csharp
var httpResponse = (HttpWebResponse)httpWebRequest.GetResponse();
using (var streamReader = new StreamReader(httpResponse.GetResponseStream()))
{
    var responseText = streamReader.ReadToEnd();
    var jsonResponse = JObject.Parse(responseText);
    // ...
}
```

The `JObject.Parse` method can be used to parse the response text into a JSON object. From there, the JSON object can be accessed and manipulated as needed.
