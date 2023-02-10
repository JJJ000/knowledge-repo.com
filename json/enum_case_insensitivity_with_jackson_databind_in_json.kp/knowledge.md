---
title: How does Jackson data binding handle enumerations in a case-insensitive manner?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Jackson databind enum case insensitive in Json can be enabled by setting the property DeserializationFeature.READ\_ENUMS\_USING\_TO\_STRING to true.
---

**Contents**

[TOC]

**Section 1: Introduction**

Jackson databind is an open-source data binding library for Java that allows developers to easily serialize and deserialize Java objects into JSON. It is a popular library for creating RESTful web services and is used in many popular frameworks such as Spring and Hibernate. Jackson databind provides a number of features, including the ability to specify how enum values should be handled when serializing and deserializing JSON.

**Section 2: Enum Case Sensitivity**

By default, Jackson databind is case-sensitive when handling enums. This means that when an enum is serialized to JSON, the value of the enum must match the exact case of the enum value. For example, if an enum has a value of “FOO”, then the JSON must also have the value of “FOO” in order for the enum to be deserialized correctly.

**Section 3: Making Enums Case-Insensitive**

Jackson databind provides an annotation, @JsonCreator, that can be used to make enum values case-insensitive. This annotation can be applied to the constructor of an enum to indicate that the constructor should be used to deserialize the JSON. The @JsonCreator annotation takes a single parameter, which is a String that indicates the name of the constructor. The String should be the exact name of the enum value that should be case-insensitive.

**Section 4: Conclusion**

Jackson databind provides a way to make enum values case-insensitive when serializing and deserializing JSON. The @JsonCreator annotation can be used to indicate which constructor should be used to deserialize the JSON. This annotation takes a single parameter, which is a String that indicates the name of the enum value that should be case-insensitive. By using this annotation, developers can ensure that their enums are deserialized correctly regardless of the case of the JSON.
