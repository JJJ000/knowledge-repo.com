---
title: What is the process for converting a jackson-encoded JavaScript date into a readable format?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the @JsonDeserialize annotation with a custom deserializer for the Date type.
---

**Contents**

[TOC]

### Section 1: Add Custom Deserializer

To deserialize a date using Jackson, you need to add a custom deserializer. This is done by creating a class that implements the JsonDeserializer interface. The class should contain a method, called deserialize, that takes a JsonParser and DeserializationContext as arguments.

### Section 2: Parse Date

Within the deserialize method, you can use the JsonParser to parse the date from the JSON. The parser will return a JsonNode object, which can be used to get the date string. The string can then be parsed into a Date object using the SimpleDateFormat class.

### Section 3: Return Date

Once the date has been parsed, it can be returned from the deserialize method. The return type of the method should be the same type as the type of the field being deserialized.

### Section 4: Register Deserializer

Finally, the custom deserializer must be registered with the ObjectMapper. This is done by calling the registerModule method on the ObjectMapper, passing in a SimpleModule containing the deserializer.
