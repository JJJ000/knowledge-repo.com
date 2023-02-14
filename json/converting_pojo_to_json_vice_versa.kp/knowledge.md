---
title: What is the process for transforming a plain old Java object into JSON and back?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: To convert POJO to JSON, use the Jackson library`s ObjectMapper.writeValueAsString() method; to convert JSON to POJO, use the ObjectMapper.readValue() method.
---

**Contents**

[TOC]

# Converting POJO to JSON

1. Create a POJO class: Create a POJO class with the necessary fields and getters and setters for each field.

2. Create an ObjectMapper: Create an instance of ObjectMapper from the Jackson library to convert the POJO to JSON.

3. Convert POJO to JSON: Use the ObjectMapper instance to convert the POJO to JSON.

# Converting JSON to POJO

1. Create a POJO class: Create a POJO class with the necessary fields and getters and setters for each field.

2. Create an ObjectMapper: Create an instance of ObjectMapper from the Jackson library to convert the JSON to POJO.

3. Convert JSON to POJO: Use the ObjectMapper instance to convert the JSON to POJO.
