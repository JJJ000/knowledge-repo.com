---
title: What is the process for converting a c# anonymous type to a JSON string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Use the Newtonsoft.Json library to serialize an anonymous type to a JSON string.
---

**Contents**

[TOC]

### Section 1: Create Anonymous Type

Anonymous types are objects that do not have a predefined type. They are typically used to store a set of values in a single object. To create an anonymous type in C#, you can use the `var` keyword along with the `new` keyword and list the properties as comma-separated values. For example:

```csharp
var person = new { Name = "John", Age = 30 };
```

### Section 2: Install JSON.NET

In order to serialize the anonymous type to a JSON string, the JSON.NET library must be installed. This can be done using NuGet. To install JSON.NET, open the NuGet Package Manager Console and type the following command:

```
Install-Package Newtonsoft.Json
```

### Section 3: Serialize Object

Once the JSON.NET library has been installed, the anonymous type can be serialized to a JSON string using the `JsonConvert.SerializeObject` method. For example:

```csharp
string jsonString = JsonConvert.SerializeObject(person);
```

### Section 4: Output

The above code will output the following JSON string:

```json
{"Name":"John","Age":30}
```
