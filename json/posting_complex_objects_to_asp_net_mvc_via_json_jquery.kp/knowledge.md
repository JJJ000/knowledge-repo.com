---
title: What is the process for sending an array of complex objects in JSON format using jquery to an ASP.NET mvc controller?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the $.ajax() method to post the array of complex objects in JSON format to the ASP.NET MVC Controller.
---

**Contents**

[TOC]

### Section 1: Create a JSON Object

The first step is to create a JSON object that contains the array of complex objects. The JSON object should be formatted as follows:

```json
{
    "complexObjects": [
        {
            "name": "object1",
            "value": "value1"
        },
        {
            "name": "object2",
            "value": "value2"
        },
        {
            "name": "object3",
            "value": "value3"
        }
    ]
}
```

### Section 2: Post the JSON Object with jQuery

Next, use the `$.ajax()` method to post the JSON object to the ASP.NET MVC Controller. The following code example shows how to post the JSON object:

```javascript
$.ajax({
    type: 'POST',
    url: '/controller/action',
    data: JSON.stringify(jsonObject),
    contentType: 'application/json; charset=utf-8',
    dataType: 'json',
    success: function (response) {
        // Do something with the response
    }
});
```

### Section 3: Deserialize the JSON Object in the Controller

In the ASP.NET MVC Controller, use the `System.Web.Script.Serialization.JavaScriptSerializer` class to deserialize the JSON object into a strongly-typed object. The following code example shows how to deserialize the JSON object:

```csharp
var serializer = new JavaScriptSerializer();
var complexObjects = serializer.Deserialize<List<ComplexObject>>(jsonObject);
```

### Section 4: Process the Deserialized Object

Finally, process the deserialized object in the ASP.NET MVC Controller as needed. The following code example shows how to process the deserialized object:

```csharp
foreach (var complexObject in complexObjects)
{
    // Do something with the complex object
}
```
