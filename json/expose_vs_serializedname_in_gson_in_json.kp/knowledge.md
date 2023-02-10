---
title: What is the difference between using @expose and @serializedname when working with gson?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: @Expose is used to indicate that a field should be included in the serialization or deserialization process, while @SerializedName is used to specify the name of the field in the JSON string.
---

**Contents**

[TOC]

### @Expose

`@Expose` is an annotation from the Gson library which is used to indicate that a field should be included in the serialization or deserialization process. This annotation can be used to control which fields are included in the JSON representation of an object.

### @SerializedName

`@SerializedName` is an annotation from the Gson library which is used to specify the name of the field to be used in the JSON representation of an object. This annotation allows developers to control the names of the fields in the JSON representation, which can be useful when dealing with legacy systems or when the JSON representation needs to match a specific format. 

### Differences

The main difference between `@Expose` and `@SerializedName` is that `@Expose` is used to control which fields are included in the serialization/deserialization process, while `@SerializedName` is used to control the names of the fields in the JSON representation.
