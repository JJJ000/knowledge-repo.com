---
title: Controller actions in ASP.NET mvc that return JSON or partial html
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Controller actions in ASP.NET MVC can return JSON or partial HTML in Json format using the JsonResult type.
---

**Contents**

[TOC]

## Returning JSON

To return JSON from an ASP.NET MVC controller action, you can use the `Json()` method. This method takes a `JsonResult` object as a parameter, which can contain data that you want to serialize into JSON. For example, the following action will return a JSON object with a single property, `message`, containing the string "Hello World!":

```csharp
public JsonResult MyJsonAction()
{
    return Json(new { message = "Hello World!" });
}
```

## Returning Partial HTML

To return partial HTML from an ASP.NET MVC controller action, you can use the `PartialView()` method. This method takes a `ViewResult` object as a parameter, which contains the name of the partial view to be rendered. For example, the following action will return the content of the partial view `MyPartialView`:

```csharp
public ViewResult MyPartialAction()
{
    return PartialView("MyPartialView");
}
```

## Returning JSON and Partial HTML

To return both JSON and partial HTML from an ASP.NET MVC controller action, you can use the `Json()` and `PartialView()` methods together. For example, the following action will return a JSON object with a single property, `partialHtml`, containing the content of the partial view `MyPartialView`:

```csharp
public JsonResult MyJsonPartialAction()
{
    var partialHtml = PartialView("MyPartialView").ToHtmlString();
    return Json(new { partialHtml = partialHtml });
}
```
