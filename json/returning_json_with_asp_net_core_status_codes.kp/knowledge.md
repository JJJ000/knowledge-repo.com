---
title: Asp.net core responds with a JSON payload and an accompanying status code
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, you can return JSON with a status code by using the JsonResult class.
---

**Contents**

[TOC]

## Section 1: Return JSON with Status Code

The most common way to return JSON with a status code is to use the `JsonResult` class from the `Microsoft.AspNetCore.Mvc` namespace. This class allows you to specify the status code as a parameter, along with the JSON data to be returned.

## Section 2: Example

The following example shows how to return a JSON response with a status code of 200 (OK):

```csharp
public JsonResult GetData()
{
    var data = GetDataFromDatabase();
    return Json(data, 200);
}
```

## Section 3: Other Options

In addition to using the `JsonResult` class, you can also use the `ObjectResult` class to return a JSON response with a status code. This class allows you to specify the status code as a parameter, along with the JSON data to be returned.

## Section 4: Example

The following example shows how to return a JSON response with a status code of 200 (OK):

```csharp
public ObjectResult GetData()
{
    var data = GetDataFromDatabase();
    return ObjectResult(data, 200);
}
```
