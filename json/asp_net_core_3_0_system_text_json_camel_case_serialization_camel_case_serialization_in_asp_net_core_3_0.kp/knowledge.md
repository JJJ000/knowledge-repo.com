---
title: Serializing in camel case using system.text.json in ASP.NET core 3.0
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: ASP.NET Core 3.0 uses System.Text.Json which supports camel case serialization by default.
---

**Contents**

[TOC]

##### Overview

ASP.NET Core 3.0 introduces a new built-in JSON serializer, System.Text.Json, which is used to serialize and deserialize objects to and from JSON. By default, System.Text.Json serializes objects in camel case. This means that property names are written in camel case, where the first letter is lowercase and the first letter of each subsequent word is uppercase.

##### Enabling Camel Case

In order to enable camel case serialization, you need to add the following code to your Startup.cs file:

```c#
services.AddMvc().AddJsonOptions(options =>
{
    options.JsonSerializerOptions.PropertyNamingPolicy = JsonNamingPolicy.CamelCase;
});
```

##### Disabling Camel Case

If you would like to disable camel case serialization, you can add the following code to your Startup.cs file:

```c#
services.AddMvc().AddJsonOptions(options =>
{
    options.JsonSerializerOptions.PropertyNamingPolicy = null;
});
```

##### Conclusion

By default, System.Text.Json serializes objects in camel case. However, you can enable or disable this behavior by adding the appropriate code to your Startup.cs file.
