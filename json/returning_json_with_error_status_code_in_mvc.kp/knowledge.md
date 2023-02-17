---
title: Send back a JSON response with an error status code in an mvc framework
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Return a JSON response with an appropriate error status code, such as 400 (Bad Request) or 500 (Internal Server Error).
---

**Contents**

[TOC]

## Section 1: Setup

To return a JSON with error status code in MVC, you need to set up the following:

1. Create a custom exception class which will be used to return the error status code.
2. Create a custom action filter attribute to handle the custom exception.
3. Configure the custom action filter attribute in your MVC application.

## Section 2: Custom Exception Class

The custom exception class should implement the `System.Exception` class and should contain the following properties:

1. Error code: This will be used to store the error status code.
2. Error message: This will be used to store the error message.

## Section 3: Custom Action Filter Attribute

The custom action filter attribute should implement the `System.Web.Mvc.ActionFilterAttribute` class and should contain the following methods:

1. OnException: This method will be used to handle the custom exception.
2. OnActionExecuted: This method will be used to return the JSON with error status code.

## Section 4: Configure Custom Action Filter Attribute

To configure the custom action filter attribute in your MVC application, you need to register it in the `Global.asax.cs` file. You can do this by adding the following code:

```csharp
GlobalFilters.Filters.Add(new CustomActionFilterAttribute());
```
