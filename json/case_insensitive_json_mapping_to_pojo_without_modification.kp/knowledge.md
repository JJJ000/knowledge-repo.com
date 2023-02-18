---
title: Mapping JSON to a pojo without altering the case sensitivity of the pojo
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: It is possible to map JSON to a POJO without changing the POJO by using a library such as Gson which supports case-insensitive deserialization.
---

**Contents**

[TOC]

### Using Jackson Annotations
Jackson provides a set of annotations which can be used to customize the JSON-POJO mapping. By using these annotations, we can control how the JSON is deserialized into the POJO.

For example, the `@JsonProperty` annotation can be used to specify the name of the JSON property that should be mapped to the POJO field. This annotation also provides an `access` parameter which can be set to `JsonProperty.Access.READ_ONLY` or `JsonProperty.Access.WRITE_ONLY` to indicate whether the field should only be read from the JSON or only written to the JSON.

The `@JsonIgnoreProperties` annotation can be used to ignore fields in the JSON which are not present in the POJO. This annotation also provides an `allowGetters` parameter which can be set to `true` to allow the JSON fields to be mapped to the getter methods of the POJO.

### Using Jackson Features
Jackson also provides a set of features which can be used to customize the JSON-POJO mapping. By using these features, we can control how the JSON is deserialized into the POJO.

For example, the `FAIL_ON_UNKNOWN_PROPERTIES` feature can be enabled to ignore fields in the JSON which are not present in the POJO. The `ACCEPT_CASE_INSENSITIVE_PROPERTIES` feature can be enabled to allow the JSON fields to be mapped to the POJO fields regardless of the case of the field names.

The `FAIL_ON_NULL_FOR_PRIMITIVES` feature can be enabled to prevent null values from being mapped to primitive fields in the POJO. The `ACCEPT_SINGLE_VALUE_AS_ARRAY` feature can be enabled to allow a single value to be deserialized as an array.

### Using Jackson Modules
Jackson also provides a set of modules which can be used to customize the JSON-POJO mapping. By using these modules, we can control how the JSON is deserialized into the POJO.

For example, the `CaseInsensitiveFieldNamesModule` module can be used to allow the JSON fields to be mapped to the POJO fields regardless of the case of the field names. The `Jdk8Module` module can be used to allow the JSON fields to be mapped to the POJO fields which are defined using the Java 8 Date/Time API.

The `ParameterNamesModule` module can be used to allow the JSON fields to be mapped to the POJO fields which are defined using Java method parameters. The `JavaTimeModule` module can be used to allow the JSON fields to be mapped to the POJO fields which are defined using the Java 8 Date/Time API.
