---
title: What is the best way to manage or disable camelcase formatting in an ASP.NET core JSON response?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: Use the JsonSerializerSettings class to set the PropertyNamingPolicy to null.
---

**Contents**

[TOC]

1. Configure JsonSerializerSettings

By default, ASP.NET Core uses the JsonSerializerSettings specified in the project's appsettings.json file. To configure the settings, add a JsonSerializerSettings section to the appsettings.json file.

2. Set the CamelCasePropertyNamesContractResolver

The CamelCasePropertyNamesContractResolver is used to control the casing of the JSON property names. To turn off camel casing, set the CamelCasePropertyNamesContractResolver to false.

3. Set the SerializerSettings

To set the SerializerSettings, use the AddJsonOptions method on the MVC services collection in the ConfigureServices method of the Startup class.

4. Configure the Response

To configure the response, use the UseMvc method on the MVC services collection in the Configure method of the Startup class. Set the JsonSerializerSettings property of the MvcOptions parameter to the settings configured in the ConfigureServices method.
