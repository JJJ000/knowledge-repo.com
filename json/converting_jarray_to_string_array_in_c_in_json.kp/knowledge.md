---
title: Convert newtonsoft.json.linq.jarray to a string array in c#
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the ToObject<string[]>() method to convert a Newtonsoft.Json.Linq.JArray to a string array in C#.
---

**Contents**

[TOC]

## Option 1

Using `Select`:

```csharp
string[] stringArray = jArray.Select(jv => (string)jv).ToArray();
```

## Option 2

Using `ToObject`:

```csharp
string[] stringArray = jArray.ToObject<string[]>();
```

## Option 3

Using `Cast`:

```csharp
string[] stringArray = jArray.Cast<string>().ToArray();
```

## Option 4

Using `ForEach`:

```csharp
string[] stringArray = new string[jArray.Count];
int index = 0;
jArray.ForEach(jv => stringArray[index++] = (string)jv);
```
