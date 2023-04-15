---
title: Reworded how to use newtonsoft.json's serializeobject method without escaping backslashes?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: By default, all backslashes in the JSON string are escaped in Newtonsoft.Json SerializeObject method.
---

**Contents**

[TOC]

## Problem

When using Newtonsoft.Json's `SerializeObject` method to serialize a string containing backslashes, they are escaped in the output, which may not be desirable in certain scenarios.

For example, serializing the string `"C:\temp\file.txt"` would result in the output `"C:\\temp\\file.txt"`.

## Solution 1: Use StringEscapeHandling.EscapeHtml

One way to prevent backslashes from being escaped is to use the `StringEscapeHandling.EscapeHtml` option when serializing the object. This option tells Newtonsoft.Json to escape special characters as HTML entities instead of using backslashes.

```csharp
var options = new JsonSerializerOptions
{
    StringEscapeHandling = StringEscapeHandling.EscapeHtml
};

var json = JsonConvert.SerializeObject(myObject, options);
```

This would result in the output `"C:\temp\file.txt"`. However, this option may not be suitable for all scenarios, as it also escapes other special characters.

## Solution 2: Use JsonTextWriter.WriteRawValue

Another way to prevent backslashes from being escaped is to manually write the property value to the JSON output using a `JsonTextWriter` and the `WriteRawValue` method.

```csharp
using (var writer = new StringWriter())
using (var jsonWriter = new JsonTextWriter(writer))
{
    jsonWriter.WriteStartObject();
    
    jsonWriter.WritePropertyName("myProperty");
    jsonWriter.WriteRawValue(@"C:\temp\file.txt");

    jsonWriter.WriteEndObject();

    var json = writer.ToString();
}
```

This would result in the output `"myProperty": "C:\temp\file.txt"`.

## Solution 3: Remove backslashes before serialization

If the backslashes are not important in the serialized data, another solution is to remove them from the string before serializing the object.

```csharp
var myObject = new { path = "C:\\temp\\file.txt" };

var json = JsonConvert.SerializeObject(new
{
    path = myObject.path.Replace("\\", "")
});
```

This would result in the output `"path": "C:temptext.txt"`. However, this solution may not be suitable if the backslashes are required in the serialized data.
