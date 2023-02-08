---
title: What is the best way to return camelcase JSON serialized by json.net from an ASP.NET mvc controller method?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Return Json(data, new JsonSerializerSettings { ContractResolver = new CamelCasePropertyNamesContractResolver() });
---

**Contents**

[TOC]

# Section 1: Setup

1. Add the following line of code to your MVC controller method:

```csharp
var jsonSerializerSettings = new JsonSerializerSettings { ContractResolver = new CamelCasePropertyNamesContractResolver() };
```

This line of code sets up the serializer settings to use the CamelCasePropertyNamesContractResolver, which will serialize JSON in camelCase format.

# Section 2: Return the JSON

2. Return the JSON using the following line of code:

```csharp
return Json(myObject, jsonSerializerSettings);
```

This line of code returns the JSON using the specified serializer settings.

# Section 3: Additional Options

3. If you want to return the JSON without using the serializer settings, you can use the following line of code:

```csharp
return JsonConvert.SerializeObject(myObject, Formatting.Indented, new JsonSerializerSettings { ContractResolver = new CamelCasePropertyNamesContractResolver() });
```

This line of code will serialize the object in camelCase format and return it as a string.

# Section 4: Conclusion

By following these steps, you can return camelCase JSON serialized by JSON.NET from ASP.NET MVC controller methods.
