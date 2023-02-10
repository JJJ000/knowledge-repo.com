---
title: What is the process for converting a joda datetime object to a JSON format using jackson?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the @JsonSerialize annotation with a custom serializer that extends JsonSerializer<DateTime>.
---

**Contents**

[TOC]

1. Add Joda Module to Jackson

In order to serialize Joda DateTime with Jackson JSON processor, it is necessary to add the Joda Module to Jackson. This can be done by including the following dependency in your `pom.xml` file:

```xml
<dependency>
    <groupId>com.fasterxml.jackson.datatype</groupId>
    <artifactId>jackson-datatype-joda</artifactId>
    <version>2.9.8</version>
</dependency>
```

2. Register Joda Module

Once the Joda Module is added, it must be registered with the Jackson ObjectMapper. This can be done by calling the `registerModule` method on the ObjectMapper, passing in an instance of the JodaModule:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.registerModule(new JodaModule());
```

3. Serialize DateTime

Once the Joda Module is registered, you can then serialize Joda DateTime objects using the Jackson ObjectMapper. The following example shows how to serialize a DateTime instance to a JSON string:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.registerModule(new JodaModule());

DateTime dateTime = new DateTime();
String json = mapper.writeValueAsString(dateTime);
```

4. Deserialize DateTime

The Jackson ObjectMapper can also be used to deserialize a JSON string into a Joda DateTime instance. The following example shows how to deserialize a DateTime instance from a JSON string:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.registerModule(new JodaModule());

String json = "{\"dateTime\":\"2020-10-01T12:00:00.000Z\"}";
DateTime dateTime = mapper.readValue(json, DateTime.class);
```
