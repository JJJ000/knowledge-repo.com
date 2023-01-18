---
title: What is the process for converting a c# object to a json string in .NET?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-18 00:00:00
updated_at: 2023-01-18 00:00:00
tldr: Use the `Newtonsoft.Json` library to serialize the C# object into a JSON string.
---

**Contents**

[TOC]

### Using the Newtonsoft.Json Library
1. Install the [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/) NuGet package.
2. Use the `JsonConvert.SerializeObject()` method to serialize the object into a JSON string.

### Using the System.Text.Json Library
1. Install the [System.Text.Json](https://www.nuget.org/packages/System.Text.Json/) NuGet package.
2. Use the `JsonSerializer.Serialize()` method to serialize the object into a JSON string.
