---
title: Exclude fields from a Java object dynamically when sending as JSON from a spring mvc application
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: We can use @JsonIgnore annotation on fields that we want to ignore while sending as JSON from Spring MVC.
---

**Contents**

[TOC]

1. Using `@JsonIgnore` Annotation:

The `@JsonIgnore` annotation can be used to ignore fields from Java object while sending as JSON from Spring MVC. This annotation can be applied to fields, getter methods or setter methods of a Java class.

2. Using `@JsonIgnoreProperties` Annotation:

The `@JsonIgnoreProperties` annotation can be used to ignore multiple fields from Java object while sending as JSON from Spring MVC. This annotation can be applied to the class itself and it takes a list of field names as parameter.

3. Using `@JsonFilter` Annotation:

The `@JsonFilter` annotation can be used to filter out fields from Java object while sending as JSON from Spring MVC. This annotation can be applied to the class itself and it takes a filter name as parameter.

4. Using `ObjectMapper`:

The `ObjectMapper` class can be used to ignore fields from Java object while sending as JSON from Spring MVC. This class has `setSerializationInclusion()` method which can be used to specify the fields to be included in the JSON output.
