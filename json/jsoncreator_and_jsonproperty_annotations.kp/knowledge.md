---
title: What is the purpose of annotating a constructor with @jsoncreator and its arguments with @jsonproperty?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: This is necessary so that Jackson knows which constructor argument corresponds to which property in the JSON.
---

**Contents**

[TOC]

#### Reason

When a constructor is annotated with @JsonCreator, its arguments must be annotated with @JsonProperty to indicate which JSON property is mapped to which constructor argument. This is necessary because the JSON keys may not match the argument names, and without this annotation, Jackson would not be able to map the JSON keys to the constructor arguments correctly.

#### Benefits

Annotating constructor arguments with @JsonProperty helps to ensure that the JSON keys are correctly mapped to the constructor arguments, allowing the object to be correctly deserialized from JSON. This eliminates the need to manually map the JSON keys to the constructor arguments, which can be time-consuming and error-prone.

#### Example

For example, consider the following JSON object:

```json
{
  "name": "John Doe",
  "age": 42
}
```

And the following Java class:

```java
public class Person {
  private String name;
  private int age;

  @JsonCreator
  public Person(@JsonProperty("name") String name, @JsonProperty("age") int age) {
    this.name = name;
    this.age = age;
  }
}
```

In this example, the constructor is annotated with @JsonCreator, and the arguments are annotated with @JsonProperty. This indicates that the JSON property "name" should be mapped to the constructor argument "name", and the JSON property "age" should be mapped to the constructor argument "age". Without the @JsonProperty annotations, Jackson would not be able to correctly map the JSON keys to the constructor arguments.
