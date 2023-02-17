---
title: Exclude a particular field from serialization using jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can use the @JsonIgnore annotation on the field to be ignored during serialization.
---

**Contents**

[TOC]

### Using @JsonIgnore

We can use the `@JsonIgnore` annotation to ignore specific fields in the serialization process. This annotation is used to mark a field as to be ignored during the serialization process.

### Example

Below is an example of how to use the `@JsonIgnore` annotation:

```java
public class Person {
    private String name;
    private int age;
    
    @JsonIgnore
    private String password;
    
    // getters and setters
}
```

In this example, the `password` field will be ignored during the serialization process.

### Using @JsonIgnoreProperties

We can also use the `@JsonIgnoreProperties` annotation to ignore specific fields in the serialization process. This annotation is used to mark a class as to be ignored during the serialization process.

### Example

Below is an example of how to use the `@JsonIgnoreProperties` annotation:

```java
@JsonIgnoreProperties({"password", "secret"})
public class Person {
    private String name;
    private int age;
    
    private String password;
    private String secret;
    
    // getters and setters
}
```

In this example, the `password` and `secret` fields will be ignored during the serialization process.
