---
title: Using .net 4.0 task pattern and httpclient, deserialize a JSON response into an array or list with readasasync
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the Task<TResult> method of the HttpClient object to read the JSON response asynchronously and deserialize it into an Array or List.
---

**Contents**

[TOC]

#### Section 1: Setting up the HTTPClient

The first step is to set up the HTTPClient with the desired URL. 

```c#
var client = new HttpClient();
client.BaseAddress = new Uri("https://example.com/api/");
```

#### Section 2: Making the Request

Once the client is set up, the next step is to make the request to the URL.

```c#
var response = await client.GetAsync("endpoint");
```

#### Section 3: Deserializing the Response

Once the response is received, the next step is to deserialize the response into an array or list.

```c#
var jsonString = await response.Content.ReadAsStringAsync();
var list = JsonConvert.DeserializeObject<List<MyObject>>(jsonString);
```

#### Section 4: Using the Deserialized List

Finally, the list can be used as desired.

```c#
foreach(var item in list)
{
    // Do something with the item
}
```
