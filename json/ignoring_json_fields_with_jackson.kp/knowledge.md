---
title: How to use Jackson to omit new fields on JSON objects?
authors:
- cool_wizard
tags:
- java
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Jackson can be configured to ignore unknown fields by setting the `FAIL_ON_UNKNOWN_PROPERTIES` flag to false.
---

**Contents**

[TOC]

### Overview

Jackson is a popular library used to parse and generate JSON objects in Java. It provides a number of features to help developers work with JSON objects, including the ability to ignore new fields that are not present in the Java class being used to parse the JSON object.

### Ignoring New Fields

When parsing a JSON object using Jackson, the library will attempt to map each field in the JSON object to a corresponding field in the Java class. If a field is present in the JSON object but not in the Java class, Jackson will throw an exception. To avoid this, Jackson provides a way to ignore new fields that are not present in the Java class.

### Setting the Feature

To enable this feature, you need to set the `FAIL_ON_UNKNOWN_PROPERTIES` feature to `false` on the `ObjectMapper` instance before parsing the JSON object. This will tell Jackson to ignore any fields that are not present in the Java class.

### Example

Here is an example of how to set the feature:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
MyClass myObject = mapper.readValue(jsonString, MyClass.class);
```

In this example, Jackson will ignore any fields in the JSON object that are not present in the `MyClass` class.
