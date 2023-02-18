---
title: Parse Java 8 localdatetime using jacksonmapper
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: You can deserialize Java 8 LocalDateTime with JacksonMapper by using the @JsonFormat annotation with the ISO\_LOCAL\_DATE\_TIME format.
---

**Contents**

[TOC]

### Section 1: Setting Up the JacksonMapper

In order to deserialize Java 8 LocalDateTime with JacksonMapper, we need to configure the JacksonMapper to recognize LocalDateTime objects. To do this, we can use the `registerModule` method of the `ObjectMapper` class. We can pass in a `JavaTimeModule` instance to the `registerModule` method, which will enable the JacksonMapper to recognize and deserialize Java 8 LocalDateTime objects.

### Section 2: Deserializing Java 8 LocalDateTime

Once the JacksonMapper is configured to recognize LocalDateTime objects, we can deserialize them from a JSON string. To do this, we can use the `readValue` method of the `ObjectMapper` class. We can pass in the JSON string and the type of the object we want to deserialize into. In this case, we would pass in `LocalDateTime.class` as the type.

### Section 3: Specifying the Date Format

By default, the JacksonMapper will use the ISO-8601 format for deserializing LocalDateTime objects. However, we can specify a different date format if needed. To do this, we can use the `setDateFormat` method of the `ObjectMapper` class. We can pass in a `DateFormat` instance, which will be used by the JacksonMapper when deserializing LocalDateTime objects.

### Section 4: Example

Here is an example of how to deserialize a Java 8 LocalDateTime object using the JacksonMapper:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.registerModule(new JavaTimeModule());
mapper.setDateFormat(new SimpleDateFormat("dd-MM-yyyy HH:mm:ss"));
LocalDateTime dateTime = mapper.readValue("\"2020-05-22T14:15:00\"", LocalDateTime.class);
```
