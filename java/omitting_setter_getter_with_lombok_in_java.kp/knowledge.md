---
title: Leaving out a setter/getter with lombok
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is not possible to omit a setter or getter when using Lombok in Java.
---

**Contents**

[TOC]

### How to Omit Setter/Getter

Lombok provides the `@Accessors` annotation to control the generation of getters and setters. You can use the `fluent` parameter of the `@Accessors` annotation to omit the setters.

```java
@Data
@Accessors(fluent = true)
public class Person {
    private String name;
    private int age;
    private double salary;
}
```

By adding the `fluent` parameter, the setters for the properties `name`, `age`, and `salary` are no longer generated.

### Benefits of Omitting Setter/Getter

The main benefit of omitting setters and getters is that it makes your code more concise and readable. Without the setters and getters, the code is simpler and easier to understand.

Another benefit of omitting setters and getters is that it reduces the amount of code that needs to be maintained. Since there are fewer methods, there is less code to maintain and debug.

### Drawbacks of Omitting Setter/Getter

The main drawback of omitting setters and getters is that it can make it more difficult to debug code. Without the setters and getters, it can be difficult to track down the source of a bug or to determine why a particular value is set.

Another potential drawback of omitting setters and getters is that it can make it more difficult to modify the code in the future. Without the setters and getters, it can be difficult to add new features or to make changes to existing code.
