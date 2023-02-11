---
title: How can I configure json.net to use the stringenumconverter for all enum types globally?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can globally set the JsonSerializerSettings.Converters property to include the StringEnumConverter.
---

**Contents**

[TOC]

## Solution

### Step 1: Create a Custom Contract Resolver

Create a custom contract resolver that inherits from the DefaultContractResolver class. This class can be used to customize the serialization and deserialization of objects.

### Step 2: Override the CreateProperties Method

Override the CreateProperties method of the custom contract resolver in order to add the StringEnumConverter to all enums.

### Step 3: Use the Custom Contract Resolver

Set the custom contract resolver to the JsonSerializerSettings object, which can then be used to serialize and deserialize objects.

### Step 4: Use the JsonSerializerSettings Object

Pass the JsonSerializerSettings object to the JsonConvert.SerializeObject and JsonConvert.DeserializeObject methods in order to serialize and deserialize objects with the custom contract resolver applied.
