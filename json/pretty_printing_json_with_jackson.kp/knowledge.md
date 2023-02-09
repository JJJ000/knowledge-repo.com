---
title: Transform a JSON string into a formatted, readable JSON output using jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Jackson can be used to pretty print a JSON String by using the ObjectMapper class`s writeValueAsString() method with the JsonGenerator.PrettyPrinter argument.
---

**Contents**

[TOC]

## Section 1: Setup

In order to use Jackson to convert a JSON string to a pretty print JSON output, you need to include the following dependencies in your project:

- Jackson Core
- Jackson Databind

## Section 2: Code

The following code snippet shows how to use Jackson to convert a JSON string to a pretty print JSON output:

```java
ObjectMapper mapper = new ObjectMapper();
String jsonString = "{\"name\":\"John\",\"age\":30,\"cars\":[\"Ford\",\"BMW\",\"Fiat\"]}";
String prettyJsonString = mapper.writerWithDefaultPrettyPrinter().writeValueAsString(jsonString);
```

## Section 3: Output

The output of the above code snippet is a pretty print JSON output as follows:

```json
{
  "name": "John",
  "age": 30,
  "cars": [
    "Ford",
    "BMW",
    "Fiat"
  ]
}
```

## Section 4: Conclusion

In conclusion, using Jackson is a convenient way to convert a JSON string to a pretty print JSON output. It is simple to setup and use, and the output is easy to read and understand.
