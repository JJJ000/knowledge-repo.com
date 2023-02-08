---
title: What is the process for creating a custom jsonconverter in json.net?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Create a class that inherits from JsonConverter and override the CanConvert, ReadJson, and WriteJson methods.
---

**Contents**

[TOC]

## Step 1: Create a Custom Converter Class

Create a class that inherits from `JsonConverter`. This class should override the `CanConvert`, `ReadJson`, and `WriteJson` methods.

## Step 2: Override the CanConvert Method

The `CanConvert` method should return `true` if the type passed to it is the type that the custom converter should handle. Otherwise, it should return `false`.

## Step 3: Override the ReadJson Method

The `ReadJson` method should deserialize the JSON string into an object of the type that the custom converter should handle.

## Step 4: Override the WriteJson Method

The `WriteJson` method should serialize the object into a JSON string.
