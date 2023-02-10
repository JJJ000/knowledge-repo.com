---
title: Converting an enum member to a JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Enum members can be serialised to JSON by using the EnumMember attribute on the member.
---

**Contents**

[TOC]

#### Serialising an Enum

Enums are a special data type that can be used to represent a set of related constants. In order to serialise an enum to JSON, the enum must be declared in a class and then the class must be serialised.

#### Using Jackson

Jackson is a popular JSON serialisation library for Java and it can be used to serialise enums. First, the enum must be declared in a class and annotated with the @JsonFormat annotation. This annotation tells Jackson how to serialise the enum.

Once the enum is declared, the class containing the enum must be annotated with the @JsonSerialize annotation. This annotation tells Jackson to serialise the class and all of its contents, including the enum.

#### Using Gson

Gson is a popular JSON serialisation library for Java and it can also be used to serialise enums. First, the enum must be declared in a class and annotated with the @SerializedName annotation. This annotation tells Gson how to serialise the enum.

Once the enum is declared, the class containing the enum must be annotated with the @Serialize annotation. This annotation tells Gson to serialise the class and all of its contents, including the enum.

#### Conclusion

Serialising an enum to JSON is a relatively straightforward process. It requires declaring the enum in a class and then annotating the class with the appropriate serialisation annotations. Jackson and Gson are two popular libraries that can be used to serialise enums.
