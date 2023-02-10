---
title: Assigning null values to unassigned fields when serializing with jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Jackson can be configured to set default values for null fields when mapping JSON data.
---

**Contents**

[TOC]

### Option 1:

Using `@JsonInclude`:

The `@JsonInclude` annotation can be used to control the serialization of properties. By setting the `Include.NON_NULL` value, Jackson will only serialize properties that are not `null`.

### Option 2:

Using `@JsonProperty`:

The `@JsonProperty` annotation can be used to set the default value of a property. This annotation can be used to set a default value to `null` fields when mapping with Jackson.

### Option 3:

Using `ObjectMapper`:

The `ObjectMapper` class can be used to set the default value of a property. This can be done by calling the `setDefaultValue` method, which takes a `Class` and a `defaultValue` parameter. This method can be used to set a default value to `null` fields when mapping with Jackson.

### Option 4:

Using `@JsonSerialize`:

The `@JsonSerialize` annotation can be used to control the serialization of a property. By setting the `JsonSerializer.None` value, Jackson will serialize the property as `null` if it is `null`. This can be used to set a default value to `null` fields when mapping with Jackson.
