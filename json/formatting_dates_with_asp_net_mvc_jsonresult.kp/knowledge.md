---
title: Formatting dates in ASP.NET mvc jsonresult
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The default date format for a JsonResult in ASP.NET MVC is the ISO 8601 format.
---

**Contents**

[TOC]

# Solution 1

When returning JsonResult from an ASP.NET MVC controller, the default date format is "yyyy-MM-ddTHH:mm:ss". This format is based on the ISO 8601 standard, which is the most widely accepted and used date format in the world.

# Solution 2

To change the date format, you can use the JsonSerializerSettings.DateFormatString property. This property allows you to specify a custom date format string that will be used when serializing dates. 

For example, to return dates in the format "MM/dd/yyyy", you can set the DateFormatString property to "MM/dd/yyyy".

# Solution 3

Another option is to use the IsoDateTimeConverter class. This class allows you to specify a custom date format string, as well as other options such as whether or not to include timezone information in the serialized dates.

# Solution 4

Finally, you can also implement a custom JsonConverter to serialize dates in a custom format. This approach is more complex, but it allows you to have full control over the serialization process.
