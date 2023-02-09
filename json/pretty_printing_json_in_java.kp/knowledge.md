---
title: Print JSON in a formatted way using java
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can pretty-print JSON in Java by using the Jackson library.
---

**Contents**

[TOC]

### Using Gson
Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object. Gson can be used to pretty print the JSON. To do so, the Gson object can be configured to output JSON that is indented properly.

### Example
Below is an example of how to use Gson to pretty print a JSON string:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";

Gson gson = new GsonBuilder().setPrettyPrinting().create();
JsonParser jp = new JsonParser();
JsonElement je = jp.parse(jsonString);
String prettyJsonString = gson.toJson(je);

System.out.println(prettyJsonString);
```

The output of the above code will be:

```json
{
  "name": "John",
  "age": 30
}
```

### Using Jackson
Jackson is another Java library used to convert Java Objects to JSON representation. It can also be used to pretty print the JSON. To do so, the ObjectMapper object can be configured to output JSON that is indented properly.

### Example
Below is an example of how to use Jackson to pretty print a JSON string:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";

ObjectMapper mapper = new ObjectMapper();
mapper.enable(SerializationFeature.INDENT_OUTPUT);

Object jsonObject = mapper.readValue(jsonString, Object.class);
String prettyJsonString = mapper.writeValueAsString(jsonObject);

System.out.println(prettyJsonString);
```

The output of the above code will be:

```json
{
  "name": "John",
  "age": 30
}
```
