---
title: What is the most effective method for invoking a JSON webservice from a .net console?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The best way to call a JSON WebService from a .NET Console is to use the HttpClient class to make an HTTP request and then deserialize the response using a JSON serializer.
---

**Contents**

[TOC]

**Section 1: Setup**

1. Create a new .NET console application in Visual Studio.
2. Add a reference to the Newtonsoft.Json NuGet package.
3. Add the following code to the Main method of the Program.cs file:

```csharp
using Newtonsoft.Json;

// Create a web request to the JSON web service
HttpWebRequest request = (HttpWebRequest)WebRequest.Create("http://example.com/webservice.json");

// Get the response from the web service
HttpWebResponse response = (HttpWebResponse)request.GetResponse();

// Read the response content
using (StreamReader reader = new StreamReader(response.GetResponseStream()))
{
    // Deserialize the JSON response
    var jsonResponse = JsonConvert.DeserializeObject<dynamic>(reader.ReadToEnd());
}
```

**Section 2: Making the Request**

1. Set the request method to GET by setting the HttpWebRequest.Method property to "GET".
2. Set the request headers by setting the HttpWebRequest.Headers property.
3. Set the request body by setting the HttpWebRequest.ContentType property.

**Section 3: Processing the Response**

1. Read the response content by using the StreamReader.ReadToEnd method.
2. Deserialize the JSON response by using the JsonConvert.DeserializeObject method.
3. Process the deserialized response object.

**Section 4: Error Handling**

1. Check the response status code by using the HttpWebResponse.StatusCode property.
2. Handle any errors that may occur by using the try-catch statement.
