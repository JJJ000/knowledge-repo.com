---
title: Unmarshalling an enum with jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Jackson can deserialize an enum by using the @JsonCreator annotation on the enum constructor.
---

**Contents**

[TOC]

1. Overview
Jackson is a popular Java library used for serializing and deserializing Java objects to and from JSON. It can be used to deserialize an enum from a JSON string.

2. Setup
The first step is to include the Jackson library in your Java project and create a class that represents the enum you wish to deserialize.

3. Deserialization
To deserialize an enum from a JSON string, you can use the ObjectMapper class in the Jackson library. The ObjectMapper class has a readValue() method which can be used to deserialize an enum from a JSON string.

4. Example
For example, if you have an enum called Color with values RED, GREEN, and BLUE, you can deserialize it from a JSON string like this:

String jsonString = "{\"color\":\"RED\"}";
ObjectMapper mapper = new ObjectMapper();
Color color = mapper.readValue(jsonString, Color.class);
