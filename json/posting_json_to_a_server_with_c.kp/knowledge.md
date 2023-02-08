---
title: What is the best way to send a JSON request to a server using c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Send a POST request with a JSON string as the body to the server.
---

**Contents**

[TOC]

1. Create the JSON Object
----------------------------

The first step is to create the JSON object. This can be done using the `Newtonsoft.Json` library. 

```c#
var jsonObject = new JObject();
jsonObject["name"] = "John Doe";
jsonObject["age"] = 30;
```

2. Create the Request
----------------------

The next step is to create the request. This can be done using the `System.Net.Http` library. 

```c#
var request = new HttpRequestMessage(HttpMethod.Post, "http://example.com/api/endpoint");
request.Content = new StringContent(jsonObject.ToString(), Encoding.UTF8, "application/json");
```

3. Send the Request
-------------------

The request can then be sent using the `HttpClient` class. 

```c#
using (var client = new HttpClient())
{
    var response = await client.SendAsync(request);
}
```

4. Handle the Response
----------------------

Finally, the response can be handled. This can be done by checking the `StatusCode` property of the response and then reading the response body. 

```c#
if (response.IsSuccessStatusCode)
{
    var responseString = await response.Content.ReadAsStringAsync();
    // Parse the response string here
}
```
