---
title: What annotation should be used to map a nested value to a property in jackson?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Using the @JsonProperty annotation, you can map a nested value to a property in the JSON object.
---

**Contents**

[TOC]

### 1. Add @JsonProperty Annotation

The @JsonProperty annotation is used to map a nested value to a property. This annotation is used to specify the name of the property in the JSON object.

### 2. Specify Nested Value in the Annotation

The nested value can be specified in the annotation by providing the full path to the value. For example, if the value of the property is located at `data.user.name`, then the annotation should be:

`@JsonProperty("data.user.name")`

### 3. Add @JsonUnwrapped Annotation

The @JsonUnwrapped annotation is used to unwrap the nested value from the JSON object. This annotation is used to avoid having to specify the full path to the value in the annotation.

### 4. Specify Property Name

The property name can be specified in the annotation by providing the name of the property. For example, if the name of the property is `name`, then the annotation should be:

`@JsonProperty("name")`
