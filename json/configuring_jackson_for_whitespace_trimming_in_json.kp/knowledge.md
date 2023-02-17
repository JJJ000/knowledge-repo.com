---
title: Is it possible to configure Jackson to remove any extra whitespace from the beginning and end of all string properties?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, Jackson can be configured to trim leading/trailing whitespace from all string properties in Json using the DeserializationFeature.ACCEPT\_EMPTY\_STRING\_AS\_NULL feature.
---

**Contents**

[TOC]

## Yes

Jackson can be configured to trim leading/trailing whitespace from all string properties in Json. This can be done by using the `JsonParser.Feature.ALLOW_TRAILING_COMMA` feature. This feature will allow Jackson to trim leading/trailing whitespace from all string properties in the Json.

## How to configure

In order to configure Jackson to trim leading/trailing whitespace from all string properties in Json, the following steps should be taken:

1. Create an instance of the `ObjectMapper` class.
2. Set the `JsonParser.Feature.ALLOW_TRAILING_COMMA` feature to `true`.
3. Call the `writeValueAsString` method on the `ObjectMapper` instance.

## Example

The following is an example of how to configure Jackson to trim leading/trailing whitespace from all string properties in Json:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.configure(JsonParser.Feature.ALLOW_TRAILING_COMMA, true);
String json = mapper.writeValueAsString(myObject);
```

## Benefits

By configuring Jackson to trim leading/trailing whitespace from all string properties in Json, users will be able to reduce the size of their Json documents and make them easier to read. Additionally, this will improve the performance of their applications by reducing the amount of data that needs to be parsed.
