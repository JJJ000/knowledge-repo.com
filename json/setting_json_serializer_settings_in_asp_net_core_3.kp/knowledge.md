---
title: What are the configuration options for a JSON serializer in ASP.NET core 3?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can set the JSON serializer settings in ASP.NET core 3 using the AddJsonOptions() method on the AddControllers() call in the ConfigureServices() method of the Startup.cs file.
---

**Contents**

[TOC]

## Section 1: Install Newtonsoft.Json

In order to set the JSON serializer settings in ASP.NET Core 3, you must first install the Newtonsoft.Json NuGet package. This can be done via the NuGet package manager in Visual Studio or using the .NET Core CLI.

## Section 2: Configure Services

Once the package is installed, you must configure the services in the Startup.cs file. This can be done by adding the following code to the ConfigureServices method:

```
services.AddControllers().AddNewtonsoftJson(options =>
{
    options.SerializerSettings.ContractResolver = new DefaultContractResolver();
    options.SerializerSettings.ReferenceLoopHandling = ReferenceLoopHandling.Ignore;
});
```

## Section 3: Set Options

The code above sets the default contract resolver and reference loop handling options, but you can also set additional options as needed. For example, you can set the MaxDepth property to control the depth of objects to serialize, or the DateFormatString property to control the format of dates.

## Section 4: Use Options

Once the options are set, they will be used whenever ASP.NET Core 3 serializes or deserializes JSON. This includes when returning data from an API endpoint or when binding data from a JSON request.
