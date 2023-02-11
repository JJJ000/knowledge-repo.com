---
title: Convert all property names in json() to lowercase in ASP.NET mvc
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The default behavior for the Json() method in ASP.NET MVC is to serialize property names in their original case.
---

**Contents**

[TOC]

**Section 1: Overview**

Json() is an extension method of the ASP.NET MVC framework that is used to serialize a .NET object into a JavaScript Object Notation (JSON) string. By default, the Json() method will serialize property names as they appear in the .NET object. This can lead to property names with mixed case, which may not be desirable for some applications.

**Section 2: Force Lowercase Property Names**

To force lowercase property names from Json(), the Json() method can be passed the JsonRequestBehavior.AllowGet parameter. This will force all property names to be serialized in lowercase.

**Section 3: Example Usage**

The following example shows how to use the JsonRequestBehavior.AllowGet parameter to force lowercase property names from Json():

```
public ActionResult GetData()
{
    var data = new { Name = "John Doe", Age = 30 };
    return Json(data, JsonRequestBehavior.AllowGet);
}
```

**Section 4: Considerations**

When using the JsonRequestBehavior.AllowGet parameter to force lowercase property names, it is important to note that the parameter should only be used when returning data that is safe to be exposed to the public.
