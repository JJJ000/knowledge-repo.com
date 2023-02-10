---
title: Retrieving JSON data in ASP.NET using webapi or mvc
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: WebAPI or MVC can be used to return JSON in ASP.NET by using the JsonResult class.
---

**Contents**

[TOC]

## WebAPI
WebAPI is a framework for building HTTP services that can be accessed from a wide range of clients, including browsers and mobile devices. It is an ideal platform for building RESTful applications on the .NET Framework. WebAPI can be used to return JSON data in ASP.NET.

To return JSON data from WebAPI, the controller must return an object of type System.Net.Http.HttpResponseMessage. The HttpResponseMessage object contains the response body and the status code of the response. The response body can be set to the JSON data that needs to be returned.

## MVC
MVC is a framework for building web applications on the .NET Framework. It is a Model-View-Controller framework that enables developers to easily create web applications that follow the MVC design pattern. MVC can be used to return JSON data in ASP.NET.

To return JSON data from MVC, the controller must return an object of type System.Web.Mvc.ActionResult. The ActionResult object contains the response body and the status code of the response. The response body can be set to the JSON data that needs to be returned.

## Conclusion
Both WebAPI and MVC can be used to return JSON data in ASP.NET. The main difference between the two is that WebAPI uses the HttpResponseMessage object to return the response, while MVC uses the ActionResult object. Both frameworks provide an easy way to return JSON data from a controller in ASP.NET.
