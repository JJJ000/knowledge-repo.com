---
title: The use of jackson's @jsonproperty annotation for kotlin data classes
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The @JsonProperty annotation can be used in Kotlin data classes to specify the name of the property in the JSON representation.
---

**Contents**

[TOC]

### Overview

The @JsonProperty annotation is used to annotate a Kotlin data class for serialization and deserialization purposes. It's part of the Jackson library, a popular library for processing JSON data in Java and Kotlin. This annotation can be used to customize the name of the property when serializing and deserializing the data class.

### Usage

The @JsonProperty annotation can be used to customize the name of the property when serializing and deserializing the data class. It takes a single parameter, which is the name of the property. For example, the following code will serialize and deserialize the property as “name” instead of “firstName”:

```kotlin
data class Person(
    @JsonProperty("name")
    val firstName: String
)
```

The @JsonProperty annotation can also be used to customize the type of the property. For example, the following code will serialize and deserialize the property as a Long instead of an Int:

```kotlin
data class Person(
    @JsonProperty(value = "age", type = Long::class)
    val age: Int
)
```

### Limitations

The @JsonProperty annotation can only be used to customize the name and type of the property. It cannot be used to customize other aspects of the serialization and deserialization process, such as the format of the data. Additionally, the @JsonProperty annotation cannot be used to customize the name of the data class itself.
