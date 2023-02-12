---
title: Send a datetime from JavaScript to a c# controller
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Pass the datetime as a string in the JSON and convert it to a DateTime object in the C# controller.
---

**Contents**

[TOC]

**Section 1 - Serializing Datetime in Javascript**

In order to pass a datetime from Javascript to C#, the datetime must first be serialized into a JSON string. This can be done using the `JSON.stringify()` method. For example, if the datetime is stored in a variable called `dateTime`, the following code can be used to serialize the datetime into a JSON string:

```js
let jsonDateTime = JSON.stringify(dateTime);
```

**Section 2 - Sending Serialized Datetime in AJAX Request**

The serialized datetime can then be sent to the C# controller in an AJAX request. The AJAX request can be configured to send the serialized datetime as part of the request body. For example, the following code can be used to send the serialized datetime in an AJAX request:

```js
$.ajax({
    type: "POST",
    url: '/Controller/Action',
    contentType: "application/json; charset=utf-8",
    data: jsonDateTime
});
```

**Section 3 - Deserializing Datetime in C# Controller**

In the C# controller, the serialized datetime can be deserialized into a `DateTime` object using the `JsonConvert.DeserializeObject()` method. For example, if the serialized datetime is stored in a variable called `jsonDateTime`, the following code can be used to deserialize the datetime into a `DateTime` object:

```c#
DateTime dateTime = JsonConvert.DeserializeObject<DateTime>(jsonDateTime);
```

**Section 4 - Using Deserialized Datetime in C# Controller**

Once the datetime is deserialized into a `DateTime` object, it can be used in the C# controller as needed. For example, the following code can be used to print the deserialized datetime to the console:

```c#
Console.WriteLine(dateTime);
```
