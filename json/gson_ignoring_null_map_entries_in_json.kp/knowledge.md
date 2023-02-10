---
title: Gson disregarding map entries with a value of null
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, Gson ignores map entries with value=null when converting to Json.
---

**Contents**

[TOC]

## Solution

### Overview
Gson is a Java library used to serialize and deserialize Java objects to (and from) JSON. By default, Gson will ignore map entries with a value of null when serializing to JSON.

### Reasons
There are two primary reasons why Gson ignores map entries with a null value:

1. To reduce the size of the resulting JSON output. By eliminating entries with null values, the resulting JSON output is smaller and more concise.

2. To adhere to the JSON standard. According to the JSON standard, only non-null values are allowed.

### Alternatives
If you wish to include map entries with a null value in the JSON output, you can use the `GsonBuilder` class to configure Gson to do so. Specifically, you can use the `GsonBuilder.serializeNulls()` method to enable serialization of null values.

### Example

```java
Gson gson = new GsonBuilder().serializeNulls().create();
String json = gson.toJson(someMap);
```
