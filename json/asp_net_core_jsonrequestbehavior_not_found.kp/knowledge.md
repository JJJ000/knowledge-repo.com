---
title: The jsonrequestbehavior identifier is not available in the current ASP.NET core context
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The JsonRequestBehavior type is not available in ASP.NET Core, as it is specific to the ASP.NET Framework.
---

**Contents**

[TOC]

**Section 1: Overview**

The error "The name 'JsonRequestBehavior' does not exist in the current context" occurs when attempting to use the JsonRequestBehavior class in an ASP.NET Core application. This error is caused by the fact that the JsonRequestBehavior class is not supported in ASP.NET Core.

**Section 2: Alternative Solutions**

Fortunately, there are alternative solutions available for developers who need to use the JsonRequestBehavior class in an ASP.NET Core application. One possible solution is to use the JsonSerializerSettings class, which provides similar functionality to the JsonRequestBehavior class.

**Section 3: Example Code**

The following code example shows how to use the JsonSerializerSettings class to achieve the same effect as the JsonRequestBehavior class:

```
var jsonSettings = new JsonSerializerSettings
{
    NullValueHandling = NullValueHandling.Ignore
};

var jsonResult = Json(data, jsonSettings);
```

**Section 4: Summary**

In summary, the error "The name 'JsonRequestBehavior' does not exist in the current context" occurs when attempting to use the JsonRequestBehavior class in an ASP.NET Core application. This error is caused by the fact that the JsonRequestBehavior class is not supported in ASP.NET Core. Fortunately, developers can use the JsonSerializerSettings class to achieve similar results.
