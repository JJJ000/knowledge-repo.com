---
title: What is the best way to retrieve a string response using retrofit in an Android application without using gson or any other library?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the responseBodyConverter method of the Retrofit Builder class to convert the response to a String.
---

**Contents**

[TOC]

### Section 1: Create a Custom Converter

Retrofit requires the use of a converter to parse the response into a Java object. To get a response as a String without using GSON or any other library, we can create a custom converter.

### Section 2: Implement the Converter

The custom converter needs to implement the Converter interface from the Retrofit library. This involves implementing the `convert(ResponseBody value)` and `convert(T value)` methods. The `convert(ResponseBody value)` method should return a String containing the response body, and the `convert(T value)` method should return the same String.

### Section 3: Register the Converter

Once the custom converter has been implemented, it needs to be registered with the Retrofit instance. This can be done by calling the `addConverterFactory()` method on the Retrofit builder.

### Section 4: Use the Converter

Once the converter is registered, it can be used to get a response as a String. This can be done by calling the `execute()` method on the Retrofit instance. The response will be parsed into a String using the custom converter.
