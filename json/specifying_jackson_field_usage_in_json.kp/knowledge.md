---
title: What is the best way to configure Jackson so that it only uses fields, preferably on a global level?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can globally configure Jackson to only use fields by setting the `FAIL\_ON\_UNKNOWN\_PROPERTIES` property to `true`.
---

**Contents**

[TOC]

1. Configure ObjectMapper

ObjectMapper is the main class of Jackson library which provides functionality for reading and writing JSON, either to and from basic POJOs (Plain Old Java Objects), or to and from a general-purpose JSON Tree Model. It can be configured to only use fields by using the `setVisibility` method.

2. Set Visibility

The `setVisibility` method takes two parameters: the visibility level and the visibility modifiers. The visibility level can be set to `JsonAutoDetect.Visibility.ANY`, `JsonAutoDetect.Visibility.NONE`, `JsonAutoDetect.Visibility.NON_PRIVATE`, or `JsonAutoDetect.Visibility.DEFAULT`. The visibility modifiers can be set to `JsonMethod.FIELD`, `JsonMethod.GETTER`, `JsonMethod.IS_GETTER`, or `JsonMethod.SETTER`. Setting the visibility level to `JsonAutoDetect.Visibility.ANY` and the visibility modifiers to `JsonMethod.FIELD` will ensure that only fields are used.

3. Create ObjectMapper

Once the visibility is set, an ObjectMapper can be created and configured. This is done by using the `ObjectMapper` class and the `setVisibility` method.

4. Use ObjectMapper

Once the ObjectMapper is configured, it can be used to read and write JSON. This is done by using the `readValue` and `writeValue` methods.
