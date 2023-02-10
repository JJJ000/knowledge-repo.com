---
title: How can I output a JSON string from an ASP.NET webapi?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Return a JSON string from an Asp.net WEBAPI by using the JsonResult class to return a serialized JSON object.
---

**Contents**

[TOC]

# Section 1: Creating a JSON String

Creating a JSON string from an Asp.net WebAPI is a relatively straightforward process. The first step is to create an object that will be used to store the data that will be serialized into a JSON string. This can be done using a `Dictionary<string, object>` or by creating a custom class.

Once an object has been created, the next step is to use the `JsonConvert.SerializeObject()` method to serialize the object into a JSON string. This method takes two parameters: the object to serialize and an optional formatting parameter. The formatting parameter allows you to specify how the JSON string should be formatted.

# Section 2: Return JSON String

Once the JSON string has been created, it can be returned from the WebAPI by using the `HttpResponseMessage` class. This class allows you to specify the status code, headers, and body of the response. To return the JSON string, the `Content` property of the `HttpResponseMessage` can be set to a `StringContent` object that contains the JSON string.

# Section 3: Setting Response Headers

When returning a JSON string from a WebAPI, it is important to set the correct response headers. This will ensure that the response is interpreted correctly by the client. The `Content-Type` header should be set to `application/json` and the `Content-Length` header should be set to the length of the JSON string.

# Section 4: Example

Below is an example of how to return a JSON string from an Asp.net WebAPI.

```
public HttpResponseMessage GetData()
{
    // Create object to serialize
    var data = new Dictionary<string, object>
    {
        { "Name", "John" },
        { "Age", 30 }
    };
    
    // Serialize object to JSON string
    var jsonString = JsonConvert.SerializeObject(data);
    
    // Create response message
    var response = new HttpResponseMessage
    {
        StatusCode = HttpStatusCode.OK,
        Content = new StringContent(jsonString, Encoding.UTF8, "application/json"),
        ContentLength = jsonString.Length
    };
    
    return response;
}
```
