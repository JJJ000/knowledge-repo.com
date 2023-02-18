---
title: Change jackson's date deserialization to the Jackson timezone
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Set the Jackson ObjectMapper`s timezone to the desired timezone before deserializing the Json.
---

**Contents**

[TOC]

## Setting Jackson Timezone

1. Create a Jackson ObjectMapper instance:
```java
ObjectMapper mapper = new ObjectMapper();
```

2. Set the TimeZone to use for deserialization:
```java
mapper.setTimeZone(TimeZone.getTimeZone("America/Los_Angeles"));
```

3. Deserialize the JSON string using the ObjectMapper instance:
```java
MyObject obj = mapper.readValue(jsonString, MyObject.class);
```

4. Access the deserialized object's Date fields to get the timezone-adjusted value:
```java
Date date = obj.getDate();
```
