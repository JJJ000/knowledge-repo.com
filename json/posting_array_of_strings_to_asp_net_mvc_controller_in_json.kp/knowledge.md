---
title: What is the best way to send an array of strings to an ASP.NET mvc controller without using a form?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use an AJAX request to post an array of strings as JSON to an ASP.NET MVC Controller.
---

**Contents**

[TOC]

1. Create the Array 

To create an array of strings, you can use the `string[]` type. For example, to create an array of three strings: 
```
string[] myArray = new string[] { "string1", "string2", "string3" };
```

2. Serialize the Array 

To serialize the array into a JSON string, you can use the `JsonConvert` class from the Newtonsoft.Json library. For example: 
```
string jsonString = JsonConvert.SerializeObject(myArray);
```

3. Send the Request 

To send the request to the ASP.NET MVC Controller, you can use the `HttpClient` class. For example: 
```
using (var client = new HttpClient())
{
    var response = await client.PostAsync("http://example.com/api/controller/action",
        new StringContent(jsonString, Encoding.UTF8, "application/json")
    );
}
```

4. Handle the Response 

To handle the response from the ASP.NET MVC Controller, you can use the `HttpResponseMessage` class. For example: 
```
if (response.IsSuccessStatusCode)
{
    var responseString = await response.Content.ReadAsStringAsync();
    // Do something with the response string
}
```
