---
title: What is the Jackson way of representing a @jsonunwrapped annotation?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The Jackson deserialization equivalent of @JsonUnwrapped is @JsonDeserialize(using = UnwrappingDeserializer.class).
---

**Contents**

[TOC]

1. Overview of @JsonUnwrapped 

@JsonUnwrapped is an annotation used to serialize/deserialize a property of a class as a standalone object. This annotation allows for the serialization/deserialization of a property as a single object, rather than as a nested object.

2. Jackson Deserialization Equivalent 

The Jackson deserialization equivalent of @JsonUnwrapped is the @JsonDeserialize annotation. This annotation allows for the deserialization of a property as a single object, rather than as a nested object.

3. Example Usage 

For example, given the following class:

```
class Person {
  String name;
  Address address;
}

class Address {
  String street;
  String city;
  String state;
  String zip;
}
```

The @JsonDeserialize annotation can be used to deserialize the address property as a single object, rather than as a nested object:

```
class Person {
  String name;
  @JsonDeserialize
  Address address;
}
```

4. Benefits 

Using the @JsonDeserialize annotation can help reduce the complexity of deserializing a property as a single object, rather than as a nested object. This simplifies the deserialization process and can improve the readability of the code.
