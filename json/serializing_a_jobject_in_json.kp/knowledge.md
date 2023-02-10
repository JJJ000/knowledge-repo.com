---
title: What is the best way to serialize a jobject without the formatting?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JObject.ToString() method.
---

**Contents**

[TOC]

### 1. Create a JObject

First, create a JObject with the desired data.

```csharp
JObject obj = new JObject();
obj["name"] = "John Doe";
obj["age"] = 30;
```

### 2. Serialize the JObject

Next, serialize the JObject using the `ToString()` method. This will return a string representation of the JObject in JSON format.

```csharp
string json = obj.ToString();
```

### 3. Remove Formatting

Finally, remove the formatting from the JSON string by replacing all whitespace characters with an empty string.

```csharp
string serialized = json.Replace(" ", "");
```

### 4. Output the Serialized JObject

The serialized JObject can now be outputted as a string.

```csharp
Console.WriteLine(serialized);
// Output: {"name":"JohnDoe","age":30}
```
