---
title: Retrieve "raw" JSON data in an ASP.NET core 2.0 web api
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Return a JsonResult from the controller action with the `Raw` option set to true.
---

**Contents**

[TOC]

1. Setting up the Web Api
--------------------------------

To return raw json in ASP.NET Core 2.0 Web Api, the first step is to set up the Web Api. This can be accomplished by creating a new ASP.NET Core 2.0 Web Api project in Visual Studio. Once the project is created, the next step is to add the necessary dependencies for the Web Api to the project. The dependencies required for a Web Api are the Microsoft.AspNetCore.Mvc and Microsoft.AspNetCore.Mvc.Formatters.Json packages.

2. Configuring the Web Api
--------------------------------

Once the dependencies are added, the next step is to configure the Web Api to return raw json. This can be accomplished by adding the following code to the ConfigureServices method of the Startup class:

```csharp
services.AddMvc()
    .AddJsonOptions(options =>
    {
        options.SerializerSettings.Formatting = Formatting.Indented;
        options.SerializerSettings.ContractResolver = new DefaultContractResolver();
    });
```

This code configures the Web Api to return json with indentation and uses the default contract resolver to serialize the json.

3. Creating the Controller
--------------------------------

The final step is to create the controller that will return the raw json. This can be accomplished by creating a new controller with the following code:

```csharp
[Route("api/[controller]")]
[ApiController]
public class MyController : ControllerBase
{
    [HttpGet]
    public IActionResult Get()
    {
        var data = new { name = "John Doe" };
        return new JsonResult(data);
    }
}
```

This code creates a controller that returns a json object with the name "John Doe".

4. Testing the Web Api
--------------------------------

Once the controller is created, the next step is to test the Web Api to ensure that it is returning raw json. This can be accomplished by running the Web Api and making a GET request to the controller. If the Web Api is configured correctly, the response should be a raw json object with the name "John Doe".
