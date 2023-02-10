---
title: What is the best way to instruct Jackson to not consider a property that I do not have control over in the source code?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use @JsonIgnore annotation on the property to tell Jackson to ignore it.
---

**Contents**

[TOC]

**Section 1: Annotation-based Solution**

One way to tell Jackson to ignore a property is to use the @JsonIgnore annotation. This annotation can be applied to the property that you want to ignore, so Jackson will not process it.

**Section 2: Configure ObjectMapper**

Another way to tell Jackson to ignore a property is to configure the ObjectMapper. The ObjectMapper can be configured to ignore certain properties by using the setSerializationInclusion() method. This method takes an Inclusion argument, which can be set to Inclusion.NON_NULL or Inclusion.NON_DEFAULT to ignore properties that are null or have default values.

**Section 3: Configure DeserializationFeature**

You can also configure the DeserializationFeature to ignore certain properties. The DeserializationFeature can be configured to ignore properties by using the setDeserializationFeature() method. This method takes a DeserializationFeature argument, which can be set to DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES to ignore properties that are not defined in the class.

**Section 4: Configure AnnotationIntrospector**

Finally, you can configure the AnnotationIntrospector to ignore certain properties. The AnnotationIntrospector can be configured to ignore properties by using the setIgnoreUnknownProperties() method. This method takes a boolean argument, which can be set to true to ignore properties that are not annotated.
