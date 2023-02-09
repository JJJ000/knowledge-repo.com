---
title: Simplest way to set access-control-allow-origin in ASP.NET mvc
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Add the following line to the Action method Response.Headers.Add(`Access-Control-Allow-Origin`, `*`);
---

**Contents**

[TOC]

## Section 1: Adding the Header

The simplest way to enable the Access-Control-Allow-Origin header in an ASP.Net MVC application is to add the following code to the `Global.asax.cs` file:

```csharp
protected void Application_BeginRequest()
{
    Response.Headers.Add("Access-Control-Allow-Origin", "*");
}
```

## Section 2: Enabling JSON

To enable JSON, the `WebApiConfig.cs` file needs to be updated to include the following code:

```csharp
public static void Register(HttpConfiguration config)
{
    config.EnableCors();
    config.Formatters.JsonFormatter.SupportedMediaTypes.Add(new MediaTypeHeaderValue("text/html"));
    config.Routes.MapHttpRoute(
        name: "DefaultApi",
        routeTemplate: "api/{controller}/{id}",
        defaults: new { id = RouteParameter.Optional }
    );
}
```

## Section 3: Setting up the Controller

In the controller, the `JsonResult` needs to be set up to allow cross-origin requests:

```csharp
public JsonResult GetData()
{
    return Json(myData, JsonRequestBehavior.AllowGet);
}
```

## Section 4: Testing the Request

To test the request, an AJAX request can be made to the controller action:

```javascript
$.ajax({
    url: '/controller/action',
    type: 'GET',
    dataType: 'json',
    success: function(data) {
        // Do something with the data
    }
});
```
