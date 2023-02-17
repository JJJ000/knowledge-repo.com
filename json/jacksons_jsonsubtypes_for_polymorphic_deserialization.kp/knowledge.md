---
title: Do we still need @jsonsubtypes for Jackson to deserialize polymorphic objects?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, Jackson`s @JsonSubTypes annotation is still necessary for polymorphic deserialization.
---

**Contents**

[TOC]

# Yes

Jackson's @JsonSubTypes annotation is still necessary for polymorphic deserialization. This annotation allows Jackson to determine the type of an object when deserializing from JSON. Without it, Jackson would not be able to determine the correct type and would instead create an instance of the parent class.

# How it Works

@JsonSubTypes is used to specify the different subtypes of a class that can be deserialized. It is used in conjunction with the @JsonTypeInfo annotation, which is used to specify the property that contains the type information. When Jackson encounters an object with a type property, it will use the @JsonSubTypes annotation to determine the type of the object and create an instance of the corresponding subclass.

# Benefits

Using @JsonSubTypes provides several benefits. It allows for a more flexible and extensible deserialization process, as new subtypes can easily be added without having to modify the existing code. It also simplifies the deserialization process, as Jackson can automatically determine the correct type without the need for any additional logic. Finally, it makes the code more maintainable, as the type information is stored in a single place and can be easily updated.
