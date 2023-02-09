---
title: How can I deserialize json.net without using the default constructor?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: You can deserialize JSON without using the default constructor by using a custom converter that implements JsonConverter.
---

**Contents**

[TOC]

#### Section 1 - Using Custom Converters

One way to deserialize JSON without using the default constructor is to use custom converters. Custom converters allow you to create custom objects from JSON strings. This approach is useful when you need to deserialize complex JSON objects that do not have a default constructor.

#### Section 2 - Implementing a Custom Deserializer

Another way to deserialize JSON without using the default constructor is to implement a custom deserializer. This requires writing custom code to map the JSON string to a custom object. This approach is useful when you need to deserialize complex JSON objects that do not have a default constructor.

#### Section 3 - Using a Third-Party Library

A third option is to use a third-party library to deserialize JSON. There are several libraries available that provide functionality for deserializing JSON without using the default constructor. This approach is useful when you need to deserialize complex JSON objects that do not have a default constructor.

#### Section 4 - Using a Custom Mapping

Finally, you can use a custom mapping to deserialize JSON without using the default constructor. This approach involves manually mapping the JSON string to the custom object. This is useful when you need to deserialize complex JSON objects that do not have a default constructor.
