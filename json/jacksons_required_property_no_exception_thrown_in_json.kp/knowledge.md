---
title: Jackson does not generate an exception when the @jsonproperty annotation is set to 'required=true'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: No, @JsonProperty(required=true) does not throw an exception, but it will cause a validation error if the associated property is missing from the JSON data.
---

**Contents**

[TOC]

## What is @JsonProperty
@JsonProperty is an annotation used in Jackson, which is a Java library used for data-binding to convert Java objects to JSON and vice-versa. It is used to mark a Java object field as a property of a JSON object. This annotation has a parameter called "required" which is used to indicate whether a field is required or not. 

## What Does @JsonProperty Do
When the "required" parameter is set to true, the field is marked as a required property of the JSON object. This means that if the field is not present in the JSON object, an exception will be thrown. If the "required" parameter is set to false, the field is not marked as a required property, and an exception will not be thrown if the field is not present in the JSON object.

## Does @JsonProperty Throw an Exception
No, @JsonProperty does not throw an exception. It is only used to mark a field as a required property of a JSON object. The exception will be thrown when the field is not present in the JSON object, not when the annotation is used.

## Conclusion
In conclusion, @JsonProperty does not throw an exception. It is only used to mark a field as a required property of a JSON object. If the field is not present in the JSON object, an exception will be thrown.
