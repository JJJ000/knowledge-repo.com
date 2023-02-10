---
title: Jackson serialization omit empty or null values
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, Jackson can be configured to ignore empty values or null values during serialization.
---

**Contents**

[TOC]

**Section 1: Overview**

Jackson serialization is a process of converting a Java object into a JSON representation. It is used to transfer data between a client and a server. Jackson provides a number of features to customize the serialization process, including the ability to ignore empty values or null values in the JSON output.

**Section 2: How to Ignore Empty Values or Nulls**

Jackson provides several options for ignoring empty values or nulls. One option is to use the @JsonInclude annotation. This annotation can be applied to a class or field, and it specifies the types of values to include in the JSON output. For example, the annotation @JsonInclude(JsonInclude.Include.NON_NULL) will tell Jackson to ignore any fields that are null when serializing the object.

Another option is to use a custom serializer. A custom serializer can be used to modify the serialization process and to explicitly ignore empty values or nulls. This can be done by overriding the serialize() method and checking for null values before writing the field to the JSON output.

**Section 3: Pros and Cons**

Ignoring empty values or nulls can be beneficial in some cases, as it can lead to smaller JSON payloads and improved performance. On the other hand, it can also lead to problems if the client and server are expecting different values. For example, if the client is expecting a field to be present but the server is ignoring it, then the client may not be able to process the response correctly.

**Section 4: Conclusion**

Jackson provides several options for ignoring empty values or nulls, including the @JsonInclude annotation and custom serializers. This can be beneficial in some cases, but it can also lead to problems if the client and server are expecting different values. It is important to carefully consider the implications of ignoring empty values or nulls before implementing this feature.
