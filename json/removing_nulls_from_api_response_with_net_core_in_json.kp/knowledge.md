---
title: Eliminate empty values from API JSON response in .net core
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can use the `NullValueHandling` property of the JsonSerializerSettings class to exclude null fields from the API JSON response.
---

**Contents**

[TOC]

**Section 1: Overview**

When creating an API that returns JSON, it is important to consider how the data will be displayed and consumed. One of the most common issues is the presence of null fields in the JSON response, which can lead to confusion and inefficiency. In this article, we will discuss how to remove null fields from an API JSON response in .NET Core.

**Section 2: Using the JsonSerializerSettings Class**

The JsonSerializerSettings class provides a way to configure the serialization of JSON objects. To remove null fields from the response, you can use the `NullValueHandling` property. This property defines how null values will be handled during serialization. Setting it to `Ignore` will cause all null fields to be omitted from the response.

**Section 3: Example Code**

The following example shows how to use the `JsonSerializerSettings` class to remove null fields from a JSON response.

```csharp
var jsonSerializerSettings = new JsonSerializerSettings
{
    NullValueHandling = NullValueHandling.Ignore
};

var jsonString = JsonConvert.SerializeObject(data, jsonSerializerSettings);
```

**Section 4: Conclusion**

In this article, we discussed how to remove null fields from an API JSON response in .NET Core. We looked at the JsonSerializerSettings class and how to use it to configure the serialization of JSON objects. With this approach, you can easily remove null fields from the response and ensure that the data is displayed in an efficient and understandable manner.
